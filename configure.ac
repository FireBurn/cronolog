dnl Template file for GNU Autoconf
dnl
dnl Process this file with autoconf to produce a configure script.
dnl
dnl Copyright (C) 1995, 1996, 1997 Free Software Foundation, Inc.
dnl
dnl This program is free software; you can redistribute it and/or modify
dnl it under the terms of the GNU General Public License as published by
dnl the Free Software Foundation; either version 2 of the License, or
dnl (at your option) any later version.
dnl
dnl This program is distributed in the hope that it will be useful,
dnl but WITHOUT ANY WARRANTY; without even the implied warranty of
dnl MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
dnl GNU General Public License for more details.
dnl
dnl You should have received a copy of the GNU General Public License
dnl along with this program; if not, write to the Free Software
dnl Foundation, Inc., 675 Mass Ave, Cambridge, MA 02139, USA.

dnl
dnl $Id: configure.ac 1671 2003-07-05 07:19:51Z andrew $
dnl


AC_REVISION($Id: configure.ac 1671 2003-07-05 07:19:51Z andrew $)

AC_INIT([cronolog], [1.6.5], [A.Ford@ford-mason.co.uk])
AC_CONFIG_SRCDIR([src/cronolog.c])
AC_CONFIG_HEADERS([config.h])

AM_INIT_AUTOMAKE([gnu dejagnu])

# Checks for programs.
AC_PROG_CC
AC_PROG_INSTALL
AC_PROG_AWK
AC_PROG_MAKE_SET
AC_PROG_RANLIB
AC_PROG_LN_S
AC_PATH_PROG([PERL], [perl])

# Checks for header files.
AC_HEADER_STDC
AC_HEADER_STAT
AC_HEADER_TIME
AC_CHECK_HEADERS([fcntl.h langinfo.h libintl.h limits.h locale.h stdlib.h string.h sys/time.h unistd.h])

# Checks for typedefs, structures, and compiler characteristics.
AC_C_CONST
AC_TYPE_MODE_T
AC_TYPE_PID_T
AC_TYPE_SIZE_T
AC_STRUCT_TM

# Checks for library functions.
AC_FUNC_MALLOC
AC_FUNC_MKTIME
AC_FUNC_LSTAT_FOLLOWS_SLASHED_SYMLINK
AC_FUNC_STAT
AC_FUNC_STRFTIME
AC_FUNC_VPRINTF
AC_CHECK_FUNCS([alarm localtime_r memset mkdir nl_langinfo putenv strcasecmp strchr strncasecmp strptime])

# ----------------------------------------------------------------------
# Custom options for documentation
# ----------------------------------------------------------------------
AC_ARG_ENABLE([docs],
  [AS_HELP_STRING([--disable-docs], [disable building all documentation])],
  [enable_docs="$enableval"],
  [enable_docs="yes"])
AM_CONDITIONAL([BUILD_DOCS], [test "x$enable_docs" = "xyes"])

AC_ARG_ENABLE([info],
  [AS_HELP_STRING([--disable-info], [disable generating texinfo documentation])],
  [enable_info="$enableval"],
  [enable_info="yes"])
AM_CONDITIONAL([BUILD_INFO], [test "x$enable_info" = "xyes"])
# ----------------------------------------------------------------------

AC_CONFIG_FILES([Makefile
                 cronolog.spec
                 doc/Makefile
                 lib/Makefile
                 src/Makefile
                 testsuite/Makefile])
AC_OUTPUT
