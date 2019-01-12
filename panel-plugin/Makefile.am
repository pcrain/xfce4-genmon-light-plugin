plugindir = $(libdir)/xfce4/panel/plugins
plugin_LTLIBRARIES = libgenmonlight.la

libgenmonlight_la_CFLAGS =						\
	-DPACKAGE_LOCALE_DIR=\"$(localedir)\"			\
	@LIBXFCE4PANEL_CFLAGS@					\
	@LIBXFCE4UI_CFLAGS@

libgenmonlight_la_LDFLAGS = 						\
	-avoid-version 						\
	-module 						\
	-no-undefined 						\
	-export-symbols-regex '^xfce_panel_module_(preinit|init|construct)'

libgenmonlight_la_LIBADD =						\
	@LIBXFCE4PANEL_LIBS@					\
	@LIBXFCE4UI_LIBS@

libgenmonlight_la_SOURCES =		\
	main.c			\
	config_gui.h		\
	config_gui.c		\
	cmdspawn.h		\
	cmdspawn.c

desktopdir = $(datadir)/xfce4/panel/plugins
desktop_DATA = genmonlight.desktop
@INTLTOOL_DESKTOP_RULE@

EXTRA_DIST = 								\
	genmonlight.desktop.in

DISTCLEANFILES =							\
	$(desktop_DATA)

