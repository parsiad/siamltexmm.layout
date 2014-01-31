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

This procedure goes over how to install the siamltexmm class and bst files for a single user.

* Move the contents of the `layouts` and `templates` directories to `~/.lyx/layouts` and `~/.lyx/templates`, respectively.
* Run

    mkdir -p ~/texmf/tex/latex/base
    mkdir -p ~/texmf/tex/latex/bibtex/bst/base
    wget http://www.siam.org/journals/tex/siamltexmm.zip
    unzip siamltexmm.zip
    mv SIAM11.clo ~/texmf/tex/latex/base/siam11.clo
    mv siamltexmm.cls subeqn.clo ~/texmf/tex/latex/base
    mv siam.bst ~/texmf/tex/latex/bibtex/bst/base

Usage
=====

I strongly recommend the use of the template file. The template file has several pieces of code without which the document may fail to compile.

* Open LyX
* Go to Tools -> Reconfigure
* Restart LyX
* Go to File -> New from Template...
* Browse to and open `~/.lyx/templates/siamltexmm.lyx`

Since the siamltexmm.cls files has several instances of the dvips option, the output in LyX must be set to DVI. Unfortunately, at the time of writing, LyX does not have a feature that allows conversion between formats post-compile, but an author wishing to produce other formats can do so by converting the resulting DVI file.

