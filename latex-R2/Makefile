
BASE	= 2020-DeepBudDetection-CEA-R2

all: pdf out
	make pdf
	make pdf

out:
	if  [ -f $(BASE).out ] ; then cp $(BASE).out tmp.out; fi ;
	sed 's/BOOKMARK/dtxmark/g;' tmp.out > x.out; mv x.out tmp.out ;

pdf:
	pdflatex -synctex=1 -interaction=nonstopmode $(BASE).tex && bibtex $(BASE)

clean:
	rm -f *.dvi *.bbl *.blg *.log *.out *.aux *.gz *.spl

###########################################################################
