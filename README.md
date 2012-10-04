CGI--Application-Ebook-Set
==========================

A set of documentation for CGI::Application and associated distributions: CGI.pm, CGI::PSGI, HTML::Template, CGI::FormBuilder and others.

## How To Produce It

* Convert POD to HTML</p>
```
pod2html --infile=Application.pm --outfile="CGI--Application.html" --noindex --podpath=.
```
*  Convert to Kindle .mobi (KF8) and EPUB .epub (EPUB3 and EPUB2)</p>
```
ebook-convert CGI--Application.html CGI--Application.mobi 
  --chapter=//h1 
  --chapter-mark=pagebreak 
  --insert-blank-line 
  --insert-blank-line-size=1 
  --smarten-punctuation 
  --mobi-file-type=new 
  --output-profile=kindle_fire 
  --level1-toc=//h:h1
  --level2-toc=//h:h2
  --level3-toc=//h:h3 
  --margin-top=0 
  --margin-right=0 
  --margin-left=0 
  --use-auto-toc 
  --language=En 
  --authors="Mark Stosberg"&"Sam Tregar" 
  --publisher="Michael Gatto - Lisantra Technologies"
```
* Rename extension from .mobi to .azw3 so the newer KF8 format works on the Kindle Touch.
