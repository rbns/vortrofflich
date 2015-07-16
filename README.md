# vortrofflich
## what?
these are some macros to be used with [heirloom-troff](https://github.com/n-t-roff/heirloom-doctools/).
troff output can look rather nice, when the right fonts are used :)

## how?
first you need to have heirloom troff in your path. then
to use these macros, set the TROFFMACS environment variable:
	export TROFFMACS=$(pwd)/tmac/
if you also want to use the fonts included here, set:
	export TROFFONTS=$(pwd)/fonts
and include this at the front of your document:
	.lc_ctype de_DE.utf8
	.fp 1 R EBGaramond12-Regular otf
	.fp 2 I EBGaramond12-Italic otf
	.fp 3 B EBGaramond12-SC otf
	.fp 4 C ConsolaMono ttf
	.fzoom C .80
note the slash at the end of TROFFMACS and the missing slash at the end of TROFFONTS.
you can test your setup with the examples.

## macros
### s
standard ms macros, with some small modifications

### s-de
like s, but with some modifications for german

### letter-de
macro for typesetting letters according to german din norms.
see the Makefile on how to get correct page numbers!

### s-beamer
ms macros customized for creating presentations. a little bit rough on
the edges, but working pretty nice so far ;). 
".so ms-beamer-header.roff" in the examples dir for setting up the 
pagesizes and fonts in the first line of your document.

