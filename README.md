# summa v0.1

A simple LaTeX class for creating invoices, geared towards European users.

## Introduction and History

The class strives to be a simple class to meet my simple needs: to create
simple invoices, optionally showing taxes, and caluclating everything
automatically. Importantly, it can handle regular and reduced tax rates in
the same invoice, which many (most) other [classes I found on CTAN](https://ctan.org/topic/invoice) can not.

It started out as a fork of 
[_rechnung.sty_](https://www.forwiss.uni-passau.de/~berberic/TeX/Rechnung/index.html)
(“Rechnung” being the German word for invoice). 
There are [other known forks](https://github.com/tomka/rechnung),
and while I am grateful for inspiration and the occasional snippet of code,
they simply implement functionality that I – as a non-German – do not need and no
longer consider “simple”. 

Also, the created invoice tables look downright ugly. (Seriously, who 
needs vertical bars? Or most hoizontal ones, for that matter?)

# Changelog

v.01 Forked from rechnung.sty. Tidyed up some code. The basics.

## Known issues / Bug / Wanted Improvements

- Remove last traces of German functions, variable names, comments etc.
- We need a configurable thousand separator, as in 100.000 vs. 100 000
  (There is code out there, just need to implement it. Inital attempt with
  siunitx have not been entirely sucessfull.)
- Only natural numbers are accepted as tax rates for now (i.e., 10, 16, 21
  etc. percent – France for one uses reduced rates of 5.5 and 2.1 percent for
  some goods or services. Similarly, Switzerland.
- Use \InvoiceLine* instead of \InvoiceLine[e]. Generally improve the handling
  of starred commands.
- An interface with babel, to choose language and/or currency (tax rates?)
  automatically
- Documentation!
- When using \Credit, store credit larger than the amount owed leads to errors

## License and Disclaimer

## Copyright

© 1998, 2001 M. G. Berberich and Ulrich Sibiller  

### LaTeX Project Public License (LPPL) v1.3

© 2022 Ingmar Greil

This work may be distributed and/or modified under the conditions of the LaTeX
Project Public License, either version 1.3 of this license or (at your
option) any later version. The latest version of this license is in
http://www.latex-project.org/lppl.txt and version 1.3 or later is part of all
distributions of LaTeX version 2005/12/01 or later.

### Legacy Copyright

The original licensing terms stated that *any modified versions of this file
must be renamed with new filenames distinct from rechnung.sty* and that
distribution was allowed, as long as the files were ditributed in its
entirety. (To cover that legal requirement, the legacy code "Original310.tgz"
is distributed as well, though not usually needed.)

#### Original German License by M.G. Berberich

Da das Paket ohne jegliche Kosten lizenziert wird, besteht keinerlei
Gewährleistung. Ich hafte weder für unmittelbar noch mittelbar entstehende
Schäden aus der Verwendung des Paketes. Ich stelle das Paket so zur
Verfügung, „wie es ist“, ohne irgendeine Gewährleistung, weder ausdrücklich
noch implizit, einschließlich, aber nicht begrenzt auf, die Tauglichkeit und
Verwendbarkeit für einen bestimmten Zweck. 

Das volle Risiko bezüglich Qualität und Leistungsfähigkeit liegt bei Ihnen.
Sollte das Programm fehlerhaft sein, übernehmen Sie die Kosten für
notwendigen Service, Reparatur oder Korrektur. Die Weitergabe dieses Pakets
ist erlaubt solange es *vollständig* weitergegeben wird. 

Änderungen an Dateien dieses Pakets sind nur zulässig wenn die Datei *vorher*
umbenannt wird, mein Copyright-Vermerk und der Haftungssausschluss erhalten
bleiben und klar ersichtlich ist, dass es sich um eine veränderte Variante
handelt.