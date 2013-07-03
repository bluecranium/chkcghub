# chkcghub: check existence, size, and checksum for bulk downloads from the Cancer Genomics Hub

## Basics
* This program was made to check the integrity of bulk sequence data downloads from the Cancer Genomics Hub (https://cghub.ucsc.edu/)
* Creating a cart using the CGHub browser (https://browser.cghub.ucsc.edu/) allows you to download an XML manifest, and this program parses that manifest to obtain file names, expected sizes, and expected md5 checksums.
* Conveniently, this same manifest can be used by CGHub's gtdownload program to do the actual downloading. The integrity can then be (re-)checked by using this script.

## Installation
Clone this repo and run the script from a BASH terminal to output usage information:

	git clone git://github.com/bluecranium/chkcghub.git
	cd chkcghub
	./chkcghub.py --help

## Usage
	# Example:
	./chkcghub.py manifest.xml

* See also the "--help" option
* Output can be piped to grep, wc, awk, etc for further interrogation