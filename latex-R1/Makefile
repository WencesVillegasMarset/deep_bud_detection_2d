
BASE	= 2020-DeepBudDetection-CEA-R1
DIR		= latex


all: pdf out
	make pdf
	make pdf

out:
	if  [ -f $(BASE).out ] ; then cp $(BASE).out tmp.out; fi ;
	sed 's/BOOKMARK/dtxmark/g;' tmp.out > x.out; mv x.out tmp.out ;

pdf:
	cp -u ../figures/*.png ./figures/
	pdflatex -synctex=1 -interaction=nonstopmode $(BASE).tex && bibtex $(BASE)

generatefigures:
	./generate_plots.sh

clean:
	rm -f *.dvi *.bbl *.blg *.log *.out *.aux *.gz *.spl $(BASE).pdf

zip:
	(cd .. && zip -r ~/$(DIR).zip $(DIR))

###########################################################################
