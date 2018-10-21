OUTDIR ?= .
ifneq ($(OUTDIR),.)
	LOUTDIR = $(OUTDIR)/thbook
else
	LOUTDIR = .
endif

all: $(LOUTDIR)/thbook.pdf $(LOUTDIR)/thbook-fr.pdf

en: $(LOUTDIR)/thbook.pdf

fr: $(LOUTDIR)/thbook-fr.pdf

$(LOUTDIR)/thbook.pdf: *.tex
	pdftex thbook.tex
	pdftex thbook.tex    
	pdftex thbook.tex
	perl ../makefile.pl rm ./thbook.log

$(LOUTDIR)/thbook-fr.pdf: *.tex
	pdftex thbook-fr.tex
	pdftex thbook-fr.tex    
	pdftex thbook-fr.tex
	perl ../makefile.pl rm ./thbook-fr.log

ifneq ($(OUTDIR),.)
	perl ../makefile.pl mv ./thbook.pdf $(LOUTDIR)
	perl ../makefile.pl mv ./thbook-fr.pdf $(LOUTDIR)
endif
    

