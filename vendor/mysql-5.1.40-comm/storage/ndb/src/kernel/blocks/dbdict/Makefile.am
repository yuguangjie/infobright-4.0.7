# Copyright (C) 2004-2005 MySQL AB
# 
# This program is free software; you can redistribute it and/or modify
# it under the terms of the GNU General Public License as published by
# the Free Software Foundation; version 2 of the License.
# 
# This program is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
# GNU General Public License for more details.
# 
# You should have received a copy of the GNU General Public License
# along with this program; if not, write to the Free Software
# Foundation, Inc., 51 Franklin St, Fifth Floor, Boston, MA  02110-1301  USA

include $(top_srcdir)/storage/ndb/config/common.mk.am
include $(top_srcdir)/storage/ndb/config/type_kernel.mk.am

LDADD +=  \
         $(top_builddir)/storage/ndb/src/common/util/libgeneral.la \
         $(top_builddir)/storage/ndb/src/common/portlib/libportlib.la \
         $(top_builddir)/dbug/libdbug.a \
         $(top_builddir)/mysys/libmysys.a \
         $(top_builddir)/strings/libmystrings.a

ndbtools_PROGRAMS = ndb_print_schema_file
ndb_print_schema_file_SOURCES = printSchemaFile.cpp
ndb_print_schema_file_LDFLAGS = @ndb_bin_am_ldflags@ \
  $(top_builddir)/storage/ndb/src/libndbclient.la \
         $(top_builddir)/dbug/libdbug.a \
         $(top_builddir)/mysys/libmysys.a \
         $(top_builddir)/strings/libmystrings.a

# Don't update the files from bitkeeper
%::SCCS/s.%
