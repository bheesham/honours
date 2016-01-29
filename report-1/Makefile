.PHONY: clean spell count

SOURCE=document.tex

# template.bib, graphics, etc.
ADDITIONAL=acm_proc_article-sp.cls sigproc.bib

NAME=$(patsubst %.tex,%,$(SOURCE))
OUTPUT=$(patsubst %.tex,%.pdf,$(SOURCE))

$(OUTPUT): $(SOURCE) $(ADDITIONAL)
	yes '' | pdflatex $(NAME); yes '' | bibtex $(NAME); \
	yes '' | pdflatex $(NAME); yes '' | pdflatex $(NAME)

count: $(SOURCE)
	texcount $<

spell: $(SOURCE)
	aspell -t -c $<

clean:
	rm -f *.aux *.bbl *log *.blg $(OUTPUT)

