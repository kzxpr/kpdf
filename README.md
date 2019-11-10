# kpdf
Counts and summarizes pages in PDF files, based on paper size and colors

UNIX-script that requires:
* ImageMagick
* Ghostscript
* bc

To run on Mac
1) Install Homebrew
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)" < /dev/null 2> /dev/null

2) Install ImageMagick through Homebrew
brew install imagemagick

3) Install Ghostscript through Homebrew
brew install ghostscript


DISCLAIMER:
The color information is based on a command in Ghostscript that simulates a print and then calculates the CMYK values. In some PDFs, black and white pages will be defined as in terms of CMYK - I've added the option "pseudo-BW" for cases where C=M=Y=K, assuming these are printing black. However, the script does not register whether it's in the same region, so a print containing precisely the same values for the four CMYK channels will also render "pseudo-BW".
