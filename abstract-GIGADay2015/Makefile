all: article

article: references.bib article.tex
	pdflatex -shell-escape  -halt-on-error article.tex
	bibtex article
	pdflatex -shell-escape  -halt-on-error article.tex
	pdflatex -shell-escape  -halt-on-error article.tex

partial:
	pdflatex -shell-escape article.tex

clean:
	rm -f *.log *.out *.aux *.bbl *.blg article.pdf


zip: article
	rm article.zip
	zip -r article.zip *.tex *.cls *.bib images article.pdf Makefile
