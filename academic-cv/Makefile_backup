.PHONY: nCV.pdf open all tarball

PDF=pdflatex --shell-escape --synctex=1

all: nCV.pdf

open:  all
	open nCV.pdf

nCV.pdf: nCV.tex citations.bib
	${PDF} nCV > output
	bibtex journal > /dev/null
	bibtex conference > /dev/null
#	bibtex media > /dev/null
	${PDF} nCV > /dev/null
	${PDF} nCV > /dev/null

tarball:
	cd .. && tar cjf CV.tz2 CV 
