.PHONY : clean

pdf:
	./knit pdf
	pandoc -s -S --biblio madsenlipo2015-replicability-archy-simulation.bib madsenlipo2015-replicability-archy-simulation.md --template=xelatex-template.tex --latex-engine=xelatex -o madsenlipo2015-replicability-archy-simulation.tex --natbib --number-sections --listings
	latexmk -pdf madsenlipo2015-replicability-archy-simulation
	open -a /Applications/Skim.app madsenlipo2015-replicability-archy-simulation.pdf


github:
	./knit github
	pandoc -s -S --biblio madsenlipo2015-replicability-archy-simulation.bib madsenlipo2015-replicability-archy-simulation.md -o madsenlipo2015-replicability-archy-simulation_github.md

md:
	pandoc -s -S --biblio madsenlipo2015-replicability-archy-simulation.bib madsenlipo2015-replicability-archy-simulation.md -o madsenlipo2015-replicability-archy-simulation.md

odt:
	./knit docx
	pandoc -s -S --biblio madsenlipo2015-replicability-archy-simulation.bib madsenlipo2015-replicability-archy-simulation.md --reference-odt=reference.odt -o madsenlipo2015-replicability-archy-simulation.odt


docx:
	./knit docx
	pandoc -s -S --biblio madsenlipo2015-replicability-archy-simulation.bib madsenlipo2015-replicability-archy-simulation.md --reference-docx=reference.docx -o madsenlipo2015-replicability-archy-simulation.docx



epub:
	./knit epub
	pandoc -s -S --biblio madsenlipo2015-replicability-archy-simulation.bib madsenlipo2015-replicability-archy-simulation.md -o madsenlipo2015-replicability-archy-simulation.epub


clean:
	latexmk -CA
	rm -rf *.log *.bbl *.blg *.out *.md *.pdf *.docx madsenlipo2015-replicability-archy-simulation.tex *.epub
