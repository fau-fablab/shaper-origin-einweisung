Shaper Origin Einweisung
========================

Einweisung des [FAU FabLab](https://fablab.fau.de) in die handgeführte CNC-Fräse Shaper Origin.

Inhalt
------

- Technische Daten, allgemeine Sicherheitshinweise, Schutzausrüstung
- Vor der ersten Benutzung, bestimmungsgemäße Verwendung, Arbeiten während Openlabs
- Frästiefe, Drehzahl, Festspannen, Tipps für Holz und Nichteisenmetalle

Download
--------

Die neueste Version aus [GitHub](https://github.com/fau-fablab/shaper-origin-einweisung) ist als PDF abrufbar:

- [Einweisung](https://brain.fablab.fau.de/build/shaper-origin-einweisung/einweisung_shaper_origin.pdf)
- [Einweisungsliste](https://brain.fablab.fau.de/build/shaper-origin-einweisung/einweisungsliste_shaper_origin.pdf)

Außerdem baut eine GitHub Action die PDFs bei jedem Push. Auf dem Hauptbranch entsteht dabei ein
[Release](https://github.com/fau-fablab/shaper-origin-einweisung/releases) mit Datums-Version (`vJJJJ.MM.TT`) und den PDFs.

Auschecken und bauen
--------------------

```bash
git clone --recursive git@github.com:fau-fablab/shaper-origin-einweisung.git
cd shaper-origin-einweisung
make
```

Die PDFs landen in `output/`. Layout, Kopf- und Fußzeile und das Logo des FAU FabLab (mit
FAU-Schriftzug) kommen aus dem Untermodul [fablab-document](https://github.com/fau-fablab/fablab-document),
das Logo wiederum aus dessen Untermodul [logo](https://github.com/fau-fablab/logo). Bei einem bestehenden
Klon die Untermodule mit `git submodule update --init --recursive` laden.

Technische Details zum Buildserver: [fau-fablab/buildserver](https://github.com/fau-fablab/buildserver)

[![Build Status](https://brain.fablab.fau.de/build/shaper-origin-einweisung/status.svg)](https://brain.fablab.fau.de/build/shaper-origin-einweisung/)
[![TODOs](https://brain.fablab.fau.de/build/shaper-origin-einweisung/status-todos.svg)](https://brain.fablab.fau.de/build/shaper-origin-einweisung/)
[![PDF bauen](https://github.com/fau-fablab/shaper-origin-einweisung/actions/workflows/pdf.yml/badge.svg)](https://github.com/fau-fablab/shaper-origin-einweisung/actions/workflows/pdf.yml)

Lizenz
------

**Noch ungeklärt:** Die Einweisung enthält Inhalte von Shapertools und aus der Festool-Einweisung.
