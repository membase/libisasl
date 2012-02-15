# libsasl
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
ACLOCAL_AMFLAGS = -I m4 --force

lib_LTLIBRARIES = libsasl.la

saslincludedir = $(includedir)/sasl

saslinclude_HEADERS = \
                     include/sasl/sasl.h \
                     include/sasl/isasl.h \
                     include/sasl/visibility.h

libsasl_la_SOURCES=src/client.c
libsasl_la_LDFLAGS=-version-info $(LIBISASL_API_CURRENT):$(LIBISASL_API_REVISION):$(LIBISASL_API_AGE) -no-undefined

