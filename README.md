# thesisdown Murdoch University

This template is a modified version of [thesisdowndmq from Thomas Fung's GitHub](https://github.com/thomas-fung/thesisdownmq).
The thesisdownmq template is inspired by the packages [thesisdown](https://github.com/ismayc/thesisdown) and [bookdown](https://github.com/rstudio/bookdown).

Under the hood, the Reed College LaTeX template.

To compile PDF documents using **R**, you are going to need to have LaTeX installed. It can be downloaded for Windows at http://http://miktex.org/download and for Mac at http://tug.org/mactex/mactex-download.html. Follow the instructions to install the necessary packages after downloading the (somewhat large) installer files. You may need to install a few extra LaTeX packages on your first attempt to knit as well.

To view an example output of the PDF document see [here](https://github.com/siobhon-egan/thesisdownMU/blob/master/_book/thesis.pdf)

### Using thesisdowndmu from Siobhon Egan's GitHub

**1) Install the latest RStudio**

I cover detailed instruction on installing R and RStudio [here](https://siobhon-egan.github.io/bioinfo-phylo/rstudio-intro.html)


**2) Install packages**

Execute the following from the R console in RStudio.

Install RMarkdown package
```
install.packages("rmarkdown")
```

You'll also need the **bookdown** and **thesisdown**
```
if (!require("remotes")) install.packages("remotes", repos = "https://cran.rstudio.org")
remotes::install_github("rstudio/bookdown")
remotes::install_github("ismayc/thesisdown")
```

**3) Download or clone this repo**

The easiest way to access and use this template is to download or clone this repo.

This can be done by going to https://github.com/siobhon-egan/thesisdownMU and selecting the green `Code` button, and select `Download zip`.

Unzip the folder and open the `thesisdownMU.Rproj`.

Alternatively in the 'terminal window' within RStudio type the following
```
git clone https://github.com/siobhon-egan/thesisdownMU.git
```

**4) Edit the `.Rmd` files**

Start by opening the `index.Rmd` file and add in all the formalities (e.g. name, supervisor, degree etc).

Note: **do not** change the name of the `index.Rmd` file.

You can remove any sections that are relavent by simply commenting them out with a `#`.

*Files*

- Files ending in `.Rmd` are the ones you edit. Start with the `index.Rmd` file and work your way through the different chapters, for example `01-chap1.Rmd` for Literature review, `02-chap2.Rmd` for Materials and Methods section etc.
- `reedthesis.cls` contains the structure and components that make up the thesis
- `template.tex` contains the LaTeX template of the thesis document
- `_bookdown.yml` outlines what files will be compiled into the final thesis document

*Directories*

- `_book/` this is where the output documents will be stored.
- `figure/` contains any images/figures that you wish to include.
- `bib/` contains the bibliography file in a `.bib` format. I use [zotero](https://www.zotero.org) (which is free!) and integrates really well with Rmarkdown, a good explaination available [here](https://christopherjunk.netlify.app/blog/2019/02/25/zotero-rmarkdown/)
- `csl/` this is a place to store the referencing template that you wish to use, offical repository for Citation Style Language (CSL) citation styles [here](https://github.com/citation-style-language/styles)
- `data/` folder to store any data you wish to use if run analysis or read data into your thesis document.


**5) Knit to PDF**

By default the document knits to PDF format.

If you want to knit the file to a different format (e.g. word or html), simply edit the `output:` section in the `index.Rmd` file.
However a word of caution is this template has been optimised for PDF output and you may find formatting issues when knitting to other formats. I am trying to work on optimising this.

Default...knit to PDF
```
output:
  thesisdownmq::thesis_pdf: default
#  thesisdown::thesis_gitbook: default
#  thesisdown::thesis_word: default
#  thesisdown::thesis_epub: default
```

Change knit to html format gitbook document
```
output:
#  thesisdownmq::thesis_pdf: default
  thesisdown::thesis_gitbook: default
#  thesisdown::thesis_word: default
#  thesisdown::thesis_epub: default
```


**6) Repeat!**

Get writing and edit the individual chapter R Markdown files as you wish and then re-run step (5) again.

***

Links to some good resources here:

- [oxforddown](https://ulyngs.github.io/oxforddown/)
- [Rmarkdown workshop](https://ulyngs.github.io/rmarkdown-workshop-2019/)
- [R Markdown the definitive guide](https://bookdown.org/yihui/rmarkdown/)
- [R for data science](https://r4ds.had.co.nz/)
- 
