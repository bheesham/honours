document.pdf: document.tex carleton/titlepage.sty
	-pdflatex document && bibtex document
	-pdflatex document
	-makeindex -s document.ist -o document.gls document.glo
	-pdflatex document
	-pdflatex document

clean:
	rm -f *.aux *.blg *.bbl \
	      *.dvi *.idx *.ist \
	      *.gls *.glo *.lof \
	      *.log *.lot *.out \
	      *.toc \
	      document.pdf
