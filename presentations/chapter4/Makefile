.PHONY: all

all: $(patsubst %.tex,%.pdf,$(wildcard *.tex))

# Compile all pdf files with and without the 'answers' displayed
%.pdf: %.tex
	pdflatex $*
	pdflatex $*
	pdflatex -jobname="$*_handout" '\PassOptionsToClass{handout}{beamer}\input{$*}'
	pdflatex -jobname="$*_handout" '\PassOptionsToClass{handout}{beamer}\input{$*}'
	pdflatex -jobname="$*_beforeClass" '\PassOptionsToClass{handout}{beamer}\input{$*}'
	pdflatex -jobname="$*_beforeClass" '\PassOptionsToClass{handout}{beamer}\input{$*}'
	$(MAKE) keepPdf

keepPdf:
	cleanTexFolder

clean:
	rm *pdf
