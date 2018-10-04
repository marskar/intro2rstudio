# Introduction to RStudio

The goal of these materials is to demonstrate a few of the many great features in RStudio.
The RStudio integrated development environment (IDE) allows you to do way more than write code in the [R programming language](https://www.r-project.org/). For example, you can make HTML slidedecks that can be put on the web, as well as PDF and powerpoint slides.

You can interact with the materials by clicking the link below.

RStudio: [![Binder](http://mybinder.org/badge.svg)](http://beta.mybinder.org/v2/gh/marskar/intro2rstudio/master?urlpath=rstudio)

Instructions for how to turn [R Markdown](https://rmarkdown.rstudio.com/lesson-1.html) (`.Rmd`) files into slides are detailed below.

One major advantage of HTML slidedecks is that you can host them on GitHub for free and share a url, instead of resorting to email or transferring files using USB drives.

Instead of using Powerpoint, Keynote, or Google Slides, I recommend you try to generate slides programmatically using the steps below.

In fact, I suggest that you avoid the horrors of Microsoft Office entirely.
- Instead of track changes in Office, use [git version control ](https://support.rstudio.com/hc/en-us/articles/200532077-Version-Control-with-Git-and-SVN)
- Instead of using Microsoft Word & Powerpoint and the doc(x) & ppt(x) formats, write [documents (including docx)](https://rmarkdown.rstudio.com/lesson-9.html) and [slideshows (including pptx)](https://rmarkdown.rstudio.com/lesson-11.html) in [R Markdown](https://rmarkdown.rstudio.com/) format and then converted into the desired output format using [RStudio](https://www.rstudio.com/products/rstudio/download/) or the [rmarkdown R package](https://github.com/rstudio/rmarkdown) in the Terminal.
- Instead of using Microsoft Excel and the xls(x) format, save tabular data as comma-separated value (csv) files. [RStudio](https://www.rstudio.com/products/rstudio/download/) has a [data viewer (can read in data from Excel, SPSS, Stata, and SAS)](https://support.rstudio.com/hc/en-us/articles/205175388-Using-the-Data-Viewer). This csv viewers is a better option for looking at data than Excel, because it does not have the ability to edit or auto-format your raw data. [Tables that are meant to be displayed in documents](https://www.markdownguide.org/extended-syntax/#tables) can also be written in [Markdown](https://www.markdownguide.org/) format instead of in Excel.

Open up a markdown file in RStudio, modify the YAML header if you want to  specify a different `output_format`, save the file and then click Preview/Knit or Press Ctrl/Cmd + Shift + K.

For revealjs and xaringan slides, you must first run `install.packages('revealjs')` and `install.packages('xaringan')` in RStudio before you can Knit (Ctrl/Cmd + Shift + K).

**You only need to install the packages once!**

You can also run install the packages and render slides from the command-line as below:

```
Rscript -e "install.packages('revealjs', repos='http://cran.us.r-project.org')"
Rscript -e "install.packages('xaringan', repos='http://cran.us.r-project.org')"
```

```
Rscript -e "rmarkdown::render('revealjs.Rmd', output_file = 'r/revealjs-r.html')"
Rscript -e "rmarkdown::render('xaringan.Rmd', output_file = 'r/xaringan.html')"
```

### Examples of HTML slides created using [RStudio](https://www.rstudio.com/products/rstudio/download/) or the [rmarkdown R package](https://github.com/rstudio/rmarkdown):
- [ioslides](/slides/ioslides.html)
- [slidy](/slides/slidy.html)
- [revealjs](/slides/revealjs.html)
- [xaringan](/slides/xaringan.html)