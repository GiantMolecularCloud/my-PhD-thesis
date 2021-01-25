# my PhD thesis

## The source code of my PhD thesis. A thesis with book tabs and a flipbook.


Much of the work of my PhD was built on an amazing ALMA data set of the emission of carbonmonoxide in the spiral galaxy NGC253.
Typically, multi-dimensional data sets like this one are visualized as a movie - obviously not possible in a printed thesis.
To still show this special data set in my thesis, I had to implement a flipbook in LaTeX.

![NGC253 flip book](https://github.com/GiantMolecularCloud/my-PhD-thesis/blob/main/preview/flipbook.gif "NGC253 flip book")

My thesis is built on an impressive thesis template: [Classic Thesis by André Miede](https://bitbucket.org/amiede/classicthesis/wiki/Home).  
Aside from a flipbook, I also added book tabs.
In this repository, you can find the complete source code of my [published thesis](https://nicokrieger.de/publications.html).  
Feel free to use this as the basis for your own thesis.


## How to use this as a template

Compiled in pdfLaTeX with TeX Live 2020 on Overleaf. Compiling locally may lead to errors due incompatible versions.

The general information (title, name, advisors, ... and setup of packages) is given in `config.tex`. 
The main file `thesis.tex` does nothing more than including the config files and actual context files (frontmatter, chapters, backmatter).
Document parts are organized in an overview file within `chapters/`, e.g. `introduction.tex`. Each content overview file includes the individual chapter files (e.g. `chapters/introduction/motivation.tex`).  
All images are in a separate directory but organize them how you like it most.
The flip book is generated from the files in `images/flipbook/`. They must be labeled with the page number. I start the flip book in the frontmatter that is labeled with roman page numbers, so the first images are labeled e.g. `flip_x.pdf`. The later pages use the normal arabic numbering. You will get all sorts of errors when the flip book images do not match the pages that require a flip book image (there might be more pages than images, so LaTeX won't find the image file it needs).  
The commands `\BeginFlip` and `\EndFlip` enable and disable the flip book. This allows to have a flip book only for the main contents but not front and backmatter.  
The text displayed by the tabs is taken from the `chaptermarks`. When starting a new chapter, also give a `\chaptermark{}`. Otherwise the displayed tab will not match the content.


## Preview

### The cover and its back:  

![cover](https://github.com/GiantMolecularCloud/my-PhD-thesis/blob/main/preview/page1.png "cover")
![cover back](https://github.com/GiantMolecularCloud/my-PhD-thesis/blob/main/preview/page2.png "cover back")


### A page with a new chapter:  

The flip book is displayed in the bottom right/left corner on the outer side of the page.
The tabs on the outer edge of the page are very useful when searching for a specific chapter.
![page starting a new chapter](https://github.com/GiantMolecularCloud/my-PhD-thesis/blob/main/preview/page3.png "page starting a new chapter")
