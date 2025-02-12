![Version](https://img.shields.io/static/v1?label=2025words&message=0.1&color=brightcolor)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
# Daily writings for 2025 in LaTeX

This is a LaTeX template for storing daily writing entries in separate files.
Each daily entry is a section in a chapter.
Each month is a separate chapter.

## Easy-Peasy Installation

`git clone` the repository or download the zip file.
Create a new project on Overleaf and drag the zip file to the upload menu.
The zip file will be unpacked in a new project.

In the menu pulldown, go to `compiler` and switch it to `LauLatex`, version `2024`.
The main document should be automatically set to `main.tex`.
The document will now be compiled in 5-10 seconds, with 12 chapters and 365 sections.

Everything will be ready to go.
You can paste your daily writing entries into the text file labeled 1January2025.tex.

## Known limitations
If your daily entries exceed 10,000 words, your project may become too large for Overleaf to compile.
In October of 2024, I ran into this limitation. 

I severely doubt that many people will run into this problem.
I have had no difficulty with compiling documents with about 1200 pages.
The pages are formatted so you can cram about 1,000 words per page.

You may need to compile it on your local computer instead.
Emacs can compile such large documents much faster than Overleaf.
Many other alternative text editors can compile LaTeX.
You can also run laulatex from the terminal.

Not all image file types are accepted (e.g., tiffs are not allowed)
PDFs, PNGs, and JPEGs work well.
The latter two types get previews in Overleaf.

## Bash function for push updates to private repository on GitHub

I developed this bash function that I can invoke anywhere to push updates I have made on Overleaf.
The updates are pushed to a private repository on GitHub.
I have a local Repository in my home directory.
I have the option of compiling the book document locally utilizing Emacs.
I can push any changes I make to the document back to Overleaf.

I have a second local Repository in the folder `~/6114BlaineMooersLabGitHubRepos`.
I push updated documents from this folder to a private Repository on GitHub.

The function below updates the local repositories and then pushes the updates to GitHub.

You will have to change the paths and set up similar directories for your project.
This script allows me to replace 23 manual operations with one command.
The script will take a optional command line argument in the form of a commit comment.


```bash
function pbook2025 () {
echo "Takes an optional commit message as a string between quotes."
echo "Example: pbook2025 'Updated entry for March 1.'"
cd ~/2025words/ov
git pull
cd /Users/blaine/6114BlaineMooersLabGitHubRepos/2025words
cp ~/2025words/ov/* .
cd ./Content
cp -R ~/2025words/ov/Content/*.tex .
cp -R ~/2025words/ov/Content/January/*.tex ./January/.
cp -R ~/2025words/ov/Content/February/*.tex ./February/.
cp -R ~/2025words/ov/Content/March/*.tex ./March/.
cp -R ~/2025words/ov/Content/April/*.tex ./April/.
cp -R ~/2025words/ov/Content/May/*.tex ./May/.
cp -R ~/2025words/ov/Content/June/*.tex ./June/.
cp -R ~/2025words/ov/Content/July/*.tex ./July/.
cp -R ~/2025words/ov/Content/August/*.tex ./August/.
cp -R ~/2025words/ov/Content/September/*.tex ./September/.
cp -R ~/2025words/ov/Content/October/*.tex ./October/.
cp -R ~/2025words/ov/Content/November/*.tex ./November/.
cp -R ~/2025words/ov/Content/December/*.tex ./December/.
cd ..
comment="${1:-Updated}"
gac ./Content "$comment"
git push
echo "Pushed the updated files for 2025words".
cd ~/2025words/ov/
pwd
}

```

|Version      | Changes                                                                                                                                   | Date                |
|:------------|:------------------------------------------------------------------------------------------------------------------------------------------|:--------------------|
| Version 0.1 |   Added badges, funding, and update table.  Initial commit.                                                                               | 2025 January 2      |
| Version 0.2 |   Updated with bash function pbook2025.                                                                                                   | 2025 February 12    |

## Sources of funding

- NIH: R01 CA242845
- NIH: R01 AI088011
- NIH: P30 CA225520 (PI: R. Mannel)
- NIH: P20 GM103640 and P30 GM145423 (PI: A. West)
