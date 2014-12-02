#konvert plantuml manual to dokuwiki + plantuml plugin

html = $(addsuffix .html,sequence usecase classes activity activity2 component state objects)
$(html) : ; wget -O $@ http://plantuml.sourceforge.net/$@

txt : $(html:.html=.txt)
%.txt : %.html
	html2text -o $@ $<
