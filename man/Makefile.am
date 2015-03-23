AUTOMAKE_OPTIONS = gnu

dist-hook:
	sphinx-build -Q -a -b man -c . . $(top_builddir)/man

check-local:
	sphinx-build -b man . $(top_builddir)/man

maintainer-clean-local:
	@rm -f *.8

dist_man_MANS = 

if ENABLE_CLIENT
include Makefile-client.am
endif

if ENABLE_SERVER
include Makefile-server.am
endif
