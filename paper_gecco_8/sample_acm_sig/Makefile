TARGETS=sig-alternate.pdf

all: ${TARGETS}

%.pdf : %.ps
	ps2pdf $< $@

%.ps : %.dvi
	dvips -t letter -o $@ $<

%.dvi : %.tex
	latex $*
	bibtex $*
	latex $*
	latex $*

clean:
	rm -f *.aux *.log *~ *.dvi *.out *.bbl *.blg *.lot *.lof *.toc ${TARGETS}
