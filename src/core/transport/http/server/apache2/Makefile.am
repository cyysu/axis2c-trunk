# Licensed to the Apache Software Foundation (ASF) under one or more
# contributor license agreements.  See the NOTICE file distributed with
# this work for additional information regarding copyright ownership.
# The ASF licenses this file to You under the Apache License, Version 2.0
# (the "License"); you may not use this file except in compliance with
# the License.  You may obtain a copy of the License at
# 
#   http://www.apache.org/licenses/LICENSE-2.0
# 
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.
lib_LTLIBRARIES = libmod_axis2.la
libmod_axis2_la_SOURCES = mod_axis2.c\
                       apache2_stream.c\
                       apache2_out_transport_info.c\
                       apache2_worker.c

AM_CFLAGS = -DLINUX=2 -D_REENTRANT -D_XOPEN_SOURCE=500 -D_BSD_SOURCE -D_SVID_SOURCE -D_GNU_SOURCE

libmod_axis2_la_LIBADD   = $(LDFLAGS) \
		     $(top_builddir)/axiom/src/om/libaxis2_axiom.la \
		     $(top_builddir)/src/core/engine/libaxis2_engine.la\
		     $(top_builddir)/util/src/libaxutil.la \
		     $(top_builddir)/src/core/transport/http/util/libaxis2_http_util.la\
		     $(top_builddir)/src/core/transport/http/common/libaxis2_http_common.la\
		     $(top_builddir)/axiom/src/parser/$(WRAPPER_DIR)/libaxis2_parser.la

libmod_axis2_la_LDFLAGS = -version-info $(VERSION_NO)

INCLUDES = -I$(top_builddir)/include \
	       -I$(top_builddir)/src/core/transport/http \
           -I$(top_builddir)/src/core/description \
           -I$(top_builddir)/src/core/context \
           -I$(top_builddir)/src/core/phaseresolver \
           -I$(top_builddir)/src/core/engine \
           -I$(top_builddir)/src/core/deployment \
           -I$(top_builddir)/axiom/include\
           -I$(top_builddir)/util/include\
            @APACHE2INC@ \
            @APRINC@

EXTRA_DIST=axis2_apache2_worker.h apache2_stream.h axis2_apache2_out_transport_info.h








