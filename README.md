siamltexmm.layout
=================

siamltexmm layout for LyX.

Use this layout if you plan on submitting to one of the following journals:

* SIAM/ASA Journal on Uncertainty Quantification (JUQ)
* SIAM Journal on Applied Dynamical Systems (SIADS)
* SIAM Journal on Financial Mathematics (SIFIN)
* SIAM Journal on Imaging Sciences (SIIMS)

Installation
============

To install siamltexmm from the SIAM website, run

	mkdir -p ~/texmf/tex/latex/base
	mkdir -p ~/texmf/tex/latex/bibtex/bst/base
	wget http://www.siam.org/journals/tex/siamltexmm.zip
	unzip siamltexmm.zip
	mv SIAM11.clo ~/texmf/tex/latex/base/siam11.clo
	mv siamltexmm.cls subeqn.clo ~/texmf/tex/latex/base
	mv siam.bst ~/texmf/tex/latex/bibtex/bst/base

To install the LyX layout files from the siamltexmm.layout repository, run

	git clone https://github.com/parsiad/siamltexmm.layout.git
	ln -s siamltexmm.layout/layouts/siamltexmm.layout $LYX/layouts/siamltexmm.layout
	ln -s siamltexmm.layout/templates/siamltexmm.lyx $LYX/templates/siamltexmm.lyx

where ```$LYX``` is the LyX configuration directory. Most configurations use ```~/.lyx```. OS X defaults to ```~/Library/Application Support/LyX-x.x/``` where ```x.x``` is the version number.

Alternatively, you can download a snapshot of the repository and move the files to the appropriate places.

Before you can use the template in LyX, you need to reconfigure LyX:

* Open LyX
* Go to Tools -> Reconfigure
* Restart LyX

Usage
=====

I strongly recommend the use of the template file. The template file has several pieces of code without which the document may fail to compile.

* Go to File -> New from Template...
* Browse to and open `~/.lyx/templates/siamltexmm.lyx`

Since the siamltexmm.cls files has several instances of the dvips option, the output in LyX must be set to DVI. Unfortunately, at the time of writing, LyX does not have a feature that allows conversion between formats post-compile, but an author wishing to produce other formats can do so by converting the resulting DVI file.

