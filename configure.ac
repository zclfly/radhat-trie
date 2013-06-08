dnl Copyright (c) 2013 Hyperbotics, Inc. <http://www.hyperbotics.com>

dnl This file is part of radhat-trie
dnl

dnl Process this file with autoconf to produce a configure script.
AC_PREREQ([2.67])
dnl Every other copy of the package version number gets its value from here
AC_INIT([radhat-trie], 0.1, harsha@meld.mn, ,[https://github.com/meld-mn/radhat-trie])
AC_CONFIG_MACRO_DIR([m4])
AM_INIT_AUTOMAKE([gnu dist-bzip2 silent-rules])
AM_SILENT_RULES(yes)

dnl create a config.h file (Automake will add -DHAVE_CONFIG_H)
AC_CONFIG_HEADERS(config.h)
AC_GNU_SOURCE

AC_SUBST(VERSION)
ISODATE=`date +%Y-%m-%d`
AC_SUBST(ISODATE)
AC_CANONICAL_HOST

AC_CONFIG_FILES([Makefile
	        src/Makefile
		src/trie/Makefile
		src/hat-trie/Makefile
		doc/Makefile
		contrib/Makefile
		contrib/aclocal/Makefile])

AC_PROG_CC
AC_PROG_LIBTOOL

dnl
dnl Word sizes...
dnl
AC_CHECK_SIZEOF(short)
AC_CHECK_SIZEOF(int)
AC_CHECK_SIZEOF(long)
AC_CHECK_SIZEOF(long long)
SIZEOF_SHORT=$ac_cv_sizeof_short
SIZEOF_INT=$ac_cv_sizeof_int
SIZEOF_LONG=$ac_cv_sizeof_long
SIZEOF_LONG_LONG=$ac_cv_sizeof_long_long
AC_SUBST(SIZEOF_SHORT)
AC_SUBST(SIZEOF_INT)
AC_SUBST(SIZEOF_LONG)
AC_SUBST(SIZEOF_LONG_LONG)

AC_CHECK_TOOL([LD],[ld])

dnl Check for pkg-config
PKG_PROG_PKG_CONFIG

AC_SUBST(AM_MAKEFLAGS)
AC_SUBST(AM_LIBTOOLFLAGS)

AC_OUTPUT
