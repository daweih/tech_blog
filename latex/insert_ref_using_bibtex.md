Insert references in article writing using bibtex
======

## Prepare the *.bib file.

![Fig. 1: Use papers to output bibtex library.](https://github.com/daweih/tech_blog/blob/master/fig/papers_output_bibtex_library.png)

Fig. 1: Use papers to output bibtex library.

![Fig. 2: Use papers to output bibtex library.](https://github.com/daweih/tech_blog/blob/master/fig/save_bibtex_library.png)

Fig. 2: Save bibtex library in the working dir of latex.


format of *.bib

example:
``
@article{Wu:2012bt,
author = {Wu, Hao and Zhang, Zhang and Hu, Songnian and Yu, Jun},
title = {{On the molecular mechanism of GC content variation among eubacterial genomes.}},
...
doi = {10.1016/j.tig.2014.05.002},
pmid = {24916172},
}
``

Pay attention that ``Wu:2012bt`` is the cite_key.

## Define the format of the reference in your article.

```tex
\bibliographystyle{natbib}
\bibliography{document}
```
Note:
- The ``document`` in ``\bibliography{}`` refer to the *.bib file.
- The ``natbib`` in ``\bibliographystyle{}`` refers to the *.bst file. See the Resources section in the article for details.

## Edit cite key in the content.
Go to the point where you want the citation to appear, and use the following: ``\cite{cite_key}``, where the cite_key corresponds to the bibitem you wish to cite.

## Produce pdf from TEX source files

```bash
latex document.tex
bibtex document.aux
latex document.tex
latex document.tex
latex document.tex
dvips document.dvi
ps2pdf document.ps

```
## Resources
- [BibTeX Style Examples](http://www.cs.stir.ac.uk/%7Ekjt/software/latex/showbst.html)
