AM_CFLAGS = -Wall \
            $(DIAG_CFLAGS) \
	    $(LIBNL_CFLAGS)

if DEBUG
AM_CFLAGS += -g
else
AM_CFLAGS += -O2
endif

requiredlibs = -lnl-3 -lnl-genl-3

if USE_GLIB
AM_CFLAGS += -DUSE_GLIB $(GLIB_CFLAGS)
requiredlibs += $(GLIB_LIBS)
endif

cnss_diag_SOURCES = cld-fwlog-netlink.c parser.c cld-diag-parser.c nan-parser.c
cnss_diag_LDADD = $(DIAG_LIBS) $(requiredlibs)

bin_PROGRAMS = cnss_diag

