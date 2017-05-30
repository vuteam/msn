SUBDIRS = countries fonts defaults extensions keymaps skin_default 

dist_pkgdata_DATA = \
	defaultsatlists.xml \
	defaultwizard.xml \
	dreampackagewizard.xml \
	encoding.conf \
	keymap.xml \
	menu.xml \
	prev.png \
	radio.mvi \
	rcpositions.xml \
	setup.xml \
	skin_default.xml \
	skin.xml \
	startwizard.xml \
	tutorialwizard.xml \
	unicable.xml \
        menuorder.bh
	
if HAVE_TEXTLCD
dist_pkgdata_DATA += skin_text.xml
else
dist_pkgdata_DATA += skin_display.xml
endif

skin_display.xml: $(srcdir)/skin_display_default.xml
	test -f $(srcdir)/skin_display_$(BOXTYPE).xml && cp $(srcdir)/skin_display_$(BOXTYPE).xml skin_display.xml || cp $(srcdir)/skin_display_default.xml skin_display.xml

skin_text.xml: $(srcdir)/skin_text_default.xml
test -f $(srcdir)/skin_text_$(BOXTYPE).xml && cp $(srcdir)/skin_text_$(BOXTYPE).xml skin_text.xml || cp $(srcdir)/skin_text_$(TEXTSKIN).xml skin_text.xml
