# Many thanks to user https://tex.stackexchange.com/users/6832/devsolar at https://tex.stackexchange.com/questions/40738/how-to-properly-make-a-latex-project



# You want latexmk to *always* run, because make does not have all the info.
# Also, include non-file targets in .PHONY so they are run regardless of any
# file of the given name existing.
.PHONY: all clean

# The first rule in a Makefile is the one executed by default ("make"). It
# should always be the "all" rule, so that "make" and "make all" are identical.
all: inkstitch_digitization_tutorial.pdf


inkstitch_digitization_tutorial.pdf:
# latexmk -pdf -pdflatex="pdflatex -interaction=nonstopmode" -use-make inkstitch_digitization_tutorial.tex
	latexmk -synctex=1 -pdflatex="pdflatex -interaction=nonstopmode" -interaction=nonstopmode -file-line-error -pdf -outdir=out

clean:
	latexmk -CA
.PHONY: all clean

inkstitch_digitization_tutorial.pdf:
	latexmk -synctex=1 -pdflatex="pdflatex -interaction=nonstopmode" -interaction=nonstopmode -file-line-error -pdf -outdir=out

clean:
	latexmk -CA
