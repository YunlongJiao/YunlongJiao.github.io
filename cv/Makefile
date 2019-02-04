filename=cv
bibname=mybib

all: ${filename}.pdf

${filename}.pdf: ${filename}.tex ${bibname}.bib
	pdflatex ${filename}
	bibtex ${filename}
	pdflatex ${filename}
	pdflatex ${filename}

read:
	open ${filename}.pdf -a Preview.app

clean:
	rm -r ${filename}.{ps,log,aux,out,dvi,bbl,blg} ${bibname}.bib.bak

.PHONY : read, clean
