# ARPACK++ documentation #

This is a TeX version of the official ARPACK++ documentation available at [www.ime.unicamp.br/~chico/arpack++](http://www.ime.unicamp.br/~chico/arpack++/). It is based on

* `arpackpp.doc`, dated May 26, 1998 (part of the [arpack++.tar.gz](http://www.ime.unicamp.br/~chico/arpack++/arpack++.tar.gz) archive) and 
* `arpackpp.ps`, dated May 1, 2000 ([arpackpp.ps.gz](http://www.ime.unicamp.br/~chico/arpack++/arpackpp.ps.gz)).

At the moment, it contains the _Users' Guide_, but not the _Function Reference_ (the appendix of the original documentation).

## License ##

The ARPACK++ documentation is published under **Creative Commons** license [BY-SA](http://creativecommons.org/licenses/by-sa/4.0/). Many thanks to Francisco Gomes and Danny Sorensen for making this possible.

## How to compile ##
The [minted](https://www.ctan.org/pkg/minted) package is used for highlighting source code. This means that Python and Pygments have to be installed to compile the tex files.

To build the *Users' Guide* PDF file, use the following commands:
    
    pdflatex -shell-escape "Users Guide.tex"
    bibtex "Users Guide"
    makeindex "Users Guide.idx"
    pdflatex -shell-escape "Users Guide.tex"
    pdflatex -shell-escape "Users Guide.tex"

## Todo ##

1. Add some kind of preface (contributors of the TeX documentation, last edit date / version, what changes were made).
2. Section 1.1 Obtaining the software:
  * Point to the GitHub version of ARPACK and ARPACK++. The links to the official homepages can stay, but it should be made clear, that those versions are no longer maintained.
  * The UMFPACK part should point to SuiteSparse, Cholmod could be mentioned.
  * Delete STL part (I don't know of any compilers that don't have native support for STL).
3. Section 1.2 Installing ARPACK++:
  * Add documentation for more up-to-date build systems (CMake).
  * Add a few notes for Windows users.
4. Section 1.5 Comparing the performance of ARPACK and ARPACK++:
  * Update with result for modern compilers.
  * Having some kind of benchmark code in the [ARPACK++](https://github.com/m-reuter/arpackpp) GitHub repository would be nice.
5. Check the bibliography (are the links available, maybe add DOIs, if available).
6. Add a more complete index.
7. Remove the reference to "Template Numerical Toolkit (TNT)" in the introduction chapter (it's not used anywhere).
8. Update all mentions of the "reference guide" or "appendix".
9. Update all references inside the documentation (text like "see chapter 2" should become pdf links).
10. Improve title page layout.