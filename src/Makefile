CAT = /usr/bin/cat
CP = /usr/bin/cp
GIT = /usr/bin/git
RM = /usr/bin/rm
SED = /usr/bin/sed

PANDOC = /usr/bin/pandoc
MD2HTML_FLAGS = --from gfm --to html

DOCS = ../docs/
MDSOURCES = blog.md
LOCAL_HTML_MDFILES = $(MDSOURCES:.md=.html)
LOCAL_HTML_FILES = $(LOCAL_HTML_MDFILES)
HTML_FILES = $(addprefix $(DOCS),$(MDSOURCES:.md=.html))

%.html: %.md
	$(PANDOC) $(MD2HTML_FLAGS) $< > $(<:.md=.tmp1);\
		$(SED) 's/^/    /' $(<:.md=.tmp1) > $(<:.md=.tmp2);\
		$(CAT) $(<:md=pre) $(<:.md=.tmp2) $(<:md=post) > $@;\
		$(RM) -f $(<:.md=.tmp1) $(<:.md=.tmp2)

default: $(LOCAL_HTML_FILES) $(HTML_FILES)

$(LOCAL_HTML_MDFILES): $(MDSOURCES)

$(HTML_FILES): $(LOCAL_HTML_FILES)	
	$(CP) $(notdir $@) $@

clean:
	$(RM) -f $(notdir $(HTML_FILES))

.PHONY: default clean html_files
