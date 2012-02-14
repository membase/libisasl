# libisasl
# Copyright (C) 2010 Membase, Inc
# All rights reserved.
#
#   Licensed under the Apache License, Version 2.0 (the "License");
#   you may not use this file except in compliance with the License.
#   You may obtain a copy of the License at
#
#       http://www.apache.org/licenses/LICENSE-2.0
#
#   Unless required by applicable law or agreed to in writing, software
#   distributed under the License is distributed on an "AS IS" BASIS,
#   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
#   See the License for the specific language governing permissions and
#   limitations under the License.
AC_PREREQ(2.60)
m4_include([m4/version.m4])
AC_INIT(sasl, VERSION_NUMBER, support@couchbase.com)
AC_CONFIG_SRCDIR([src/client.c])
AC_CONFIG_AUX_DIR(config)
AC_USE_SYSTEM_EXTENSIONS
AM_INIT_AUTOMAKE(subdir-objects)
AC_PROG_CC
AM_PROG_CC_C_O
AC_PROG_LN_S
AC_DISABLE_STATIC
AC_PROG_LIBTOOL
AM_CONFIG_HEADER([src/config.h])
AC_CONFIG_MACRO_DIR([m4])

# the malloc tests seems to be broken for cross compilation.. ignore them
ac_cv_func_malloc_0_nonnull=yes
ac_cv_func_realloc_0_nonnull=yes

COUCHBASE_GENERIC_COMPILER(c99)
AM_CPPFLAGS="$AM_CPPFLAGS -I\${top_srcdir}/include -DLIBISASL_INTERNAL"

#
# To ensure that we don't break applications in mysterious ways we need
# to version our library. For a detailed description, check out:
# http://www.gnu.org/software/libtool/manual/libtool.html#Libtool-versioning
#
LIBISASL_API_CURRENT=1
LIBISASL_API_REVISION=0
LIBISASL_API_AGE=0
AC_SUBST(LIBISASL_API_CURRENT)
AC_SUBST(LIBISASL_API_REVISION)
AC_SUBST(LIBISASL_API_AGE)


dnl ----------------------------------------------------------------------------

AC_CONFIG_FILES(Makefile)
AC_OUTPUT
