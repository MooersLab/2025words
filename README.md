![Version](https://img.shields.io/static/v1?label=matplotlib-voice-in&message=0.0&color=brightcolor)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
# Daily writings for 2025 in LaTeX

This is a LaTeX template for storing daily writing entries in separate files.
Each daily entry is a section in a chapter.
Each month is a separate chapter.

## Easy-Peasy Installation

Get clone the repository or download the zip file.
Create a new project on Overleaf and drag the zip file to the upload menu.
The zip file will be unpacked in a new project.

In the menu pulldown, go to compiler and switch it to LauLatex, version 2024.
The main document should be automatically set to main.tex.
The doument will now compile in 5-10s with 12 chapters and 365 sections.

Everything will be ready to go.
You can paste your daily writing entries into the text file labeled 1January2025.tex.

## Known imitations
If you have entries that are much longer than 10,000 words per day, you may run into your project becoming too large for Overleaf to compile it.
In October of 2024, I ran into this limitation. 

I severely doubt that many people will run into this problem.
I have had no difficulty with compiling documents with about 1200 pages.
The pages are formatted so you can cram about 1,000 words per page.

You may need to compile it on your local computer instead.
Emacs can compile such large documents much faster than Overleaf.
There are many other alternative text editors that can compile LaTeX.
You can also run laulatex from the terminal.

No all image file types are accepted (e.g., tiffs are not allowed)
PDFs, PNGs, and JPEGs work well.
The latter two have previews.

|Version      | Changes                                                                                                                                  | Date                 |
|:-----------|:------------------------------------------------------------------------------------------------------------------------------------------|:--------------------|
| Version 0.1 |   Added badges, funding, and update table.  Initial commit.                                                                              | 2025 January 2  |

## Sources of funding

- NIH: R01 CA242845
- NIH: R01 AI088011
- NIH: P30 CA225520 (PI: R. Mannel)
- NIH: P20 GM103640 and P30 GM145423 (PI: A. West)
