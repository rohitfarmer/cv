.PHONY: nCV.pdf open all 

PDF=pdflatex --shell-escape --synctex=1

all: nCV.pdf

open:  all
	open nCV.pdf

nCV.pdf: nCV.tex citations.bib
	${PDF} nCV > output
	bibtex journal > /dev/null
	${PDF} nCV > /dev/null
	${PDF} nCV > /dev/null
