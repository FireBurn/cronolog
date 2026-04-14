## Process this file with automake to create Makefile.in
## $Id: Makefile.am 1671 2003-07-05 07:19:51Z andrew $

AUTOMAKE_OPTIONS  = gnu dejagnu
EXTRA_DIST        = cronolog.spec

if BUILD_DOCS
DOC_SUBDIR = doc
endif

SUBDIRS           = lib src $(DOC_SUBDIR) testsuite

# DIST_SUBDIRS ensures 'make dist' still knows about the doc folder
DIST_SUBDIRS      = lib src doc testsuite
