# vim: set noexpandtab ts=8 sts=8 sw=8:

# Define a C macro LOCALEDIR indicating where catalogs 
# will be installed.

bin_PROGRAMS += %reldir%/tilda

%canon_reldir%_tilda_CPPFLAGS = \
    $(AM_CPPFLAGS) \
    -DDATADIR='"$(datadir)"' \
    -DLOCALEDIR='"$(localedir)"' \
    -DPKGDATADIR='"$(pkgdatadir)"'

# Keep the headers here so that make dist-bzip2 works
%canon_reldir%_tilda_SOURCES = src/callback_func.h src/callback_func.c \
		src/configsys.h src/configsys.c \
		src/debug.h \
		src/eggaccelerators.h src/eggaccelerators.c \
		src/key_grabber.h src/key_grabber.c \
		src/tilda.h src/tilda.c \
		src/tilda_terminal.h src/tilda_terminal.c \
		src/tilda_window.h src/tilda_window.c \
		src/tomboykeybinder.h src/tomboykeybinder.c \
		src/wizard.h src/wizard.c \
		src/xerror.h src/xerror.c

%canon_reldir%_tilda_CFLAGS = $(AM_CFLAGS) \
		$(GTK_CFLAGS) \
		$(LIBGLADE_CFLAGS) \
		$(VTE_CFLAGS) \
		$(LIBCONFUSE_CFLAGS)

%canon_reldir%_tilda_LDFLAGS = $(AM_LDFLAGS) \
		$(GTK_LDFLAGS) \
		$(LIBGLADE_LDFLAGS) \
		$(VTE_LDFLAGS) \
		$(LIBCONFUSE_LDFLAGS) \
		-Wl,--as-needed

%canon_reldir%_tilda_LDADD = $(AM_LDADD) \
		$(GTK_LIBS) \
		$(LIBGLADE_LIBS) \
		$(VTE_LIBS) \
		$(LIBCONFUSE_LIBS) \
		$(LTLIBINTL) \
		$(LEXLIB)
