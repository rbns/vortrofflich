ms:
	troff -x3 -ms ms.roff | dpost > ms.ps
	ps2pdf ms.ps	

letter:
	troff -mletter-de -Tps letter-de.roff > /dev/null
	troff -rtotal=$(shell cat /tmp/de-letter-pagecount) -mletter-de -Tps letter-de.roff | dpost > letter-de.ps
	ps2pdf letter-de.ps
