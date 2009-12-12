rebuild: StoryDSA.pdf

draft: StoryDSA_draft.pdf

final: StoryDSA_final.pdf

all: StoryDSA_final.pdf StoryDSA_draft.pdf

clean:
	rm -f StoryDSA.aux StoryDSA.idx StoryDSA.ilg StoryDSA.ind StoryDSA.log StoryDSA.mst StoryDSA.toc StoryDSA.top StoryDSA.tui StoryDSA_Mode.tex StoryDSA_draft.pdf StoryDSA_final.pdf StoryDSA.pdf
	rm -f include/*.aux

StoryDSA.pdf: *.tex include/*.tex
	pdflatex StoryDSA

StoryDSA_draft.pdf: *.tex include/*.tex
	cp StoryDSA_Mode_draft.tex StoryDSA_Mode.tex
	pdflatex StoryDSA
	makeindex StoryDSA
	pdflatex StoryDSA
	cp StoryDSA.pdf StoryDSA_draft.pdf

StoryDSA_final.pdf: *.tex include/*.tex
	cp StoryDSA_Mode_final.tex StoryDSA_Mode.tex
	pdflatex StoryDSA
	makeindex StoryDSA
	pdflatex StoryDSA
	cp StoryDSA.pdf StoryDSA_final.pdf
