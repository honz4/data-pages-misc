#konvert plantuml manual to dokuwiki + plantuml plugin
help : ; @cat Makefile

html = $(addsuffix .html,sequence usecase classes activity activity2 component state objects)
html = salt.html
html = creole.html
html = commons.html
html = skinparam.html

html :: $(addprefix ./html/,$(html))
html :: FORCE
$(addprefix ./html/,$(html)) : ; wget -O $@ http://plantuml.sourceforge.net/$(notdir $@)

txt : $(html:.html=.txt)

%.txt : ./html/%.html
	html2text -o $@ $<

FORCE : ;
