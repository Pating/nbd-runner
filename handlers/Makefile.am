lib_LTLIBRARIES =

if WITH_GLUSTER
lib_LTLIBRARIES += libgluster_handler.la

libgluster_handler_la_LIBADD = $(GFAPI_LIBS) $(GLIB2_LIBS)                  \
                               $(top_builddir)/utils/libutils.la

libgluster_handler_la_LDFLAGS = -avoid-version -rdynamic

libgluster_handler_la_CFLAGS = $(GFAPI_CFLAGS) -I$(top_builddir)/           \
                               $(GLIB2_CFLAGS) -I$(top_builddir)/daemon     \
                               $(TIRPC_CFLAGS) -I$(top_srcdir)/rpc          \
                               -I$(top_srcdir)/utils

libgluster_handler_la_SOURCES = gluster.c
endif

if WITH_AZBLK
lib_LTLIBRARIES += libazblk_handler.la

libazblk_handler_la_LIBADD = $(UV_LIBS) $(GLIB2_LIBS) $(CURL_LIBS)          \
                             $(top_builddir)/utils/libutils.la

libazblk_handler_la_LDFLAGS = -avoid-version -rdynamic

libazblk_handler_la_CFLAGS = $(GLIB2_CFLAGS) $(CURL_CFLAGS) $(UV_CFLAGS)    \
                             $(TIRPC_CFLAGS) -I$(top_builddir)/daemon       \
                             -I$(top_srcdir)/rpc -I$(top_srcdir)/utils      \
                             -I$(top_builddir)/

libazblk_handler_la_SOURCES = azblk.c
endif

DISTCLEANFILES = Makefile.in

CLEANFILES = *~
