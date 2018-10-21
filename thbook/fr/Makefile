OUTDIR ?= .
ifneq ($(OUTDIR),.)
LOUTDIR = $(OUTDIR)/thbook
else
LOUTDIR = .
endif

all: $(LOUTDIR)/thbook-fr.pdf

$(LOUTDIR)/thbook-fr.pdf: *.tex
	pdftex thbook-fr.tex
	pdftex thbook-fr.tex    
	pdftex thbook-fr.tex
	perl ../../makefile.pl rm ./thbook-fr.log
ifneq ($(OUTDIR),.)
	perl ../../makefile.pl mv ./thbook-fr.pdf $(LOUTDIR)
endif
    

