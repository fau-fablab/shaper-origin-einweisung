Shaper Origin Einweisung
========================

Einweisung des [FAU FabLab](https://fablab.fau.de) in die handgeführte CNC-Fräse Shaper Origin.

Inhalt
------

- Regeln und Sicherheit, Betriebsanweisung BA-SO-01 (Aushang beim Origin, noch Entwurf)
- So funktioniert der Origin, Bedienelemente (schematische Zeichnung), Anleitung des Herstellers
- Vorbereitung: Checkliste, Schutzausrüstung, Material, Absaugung, Werkstück befestigen, ShaperTape kleben und scannen
- Einstellungen: Fräser wechseln, Z-Touch und Frästiefe, Drehzahl
- Fräsen: Entwurf, Schnittarten und Offset, Ablauf Schritt für Schritt, Bildschirm, Fräsrichtung, Holz, Nichteisenmetalle, Verbotsliste, OpenLabs
- Nach dem Fräsen, Infos für Betreuer: typische Fehler, Pflege und Prüfung

Download
--------

Die neueste Version aus [GitHub](https://github.com/fau-fablab/shaper-origin-einweisung) ist als PDF abrufbar:

- [Einweisung](https://brain.fablab.fau.de/build/shaper-origin-einweisung/einweisung_shaper_origin.pdf)
- [Einweisungsliste](https://brain.fablab.fau.de/build/shaper-origin-einweisung/einweisungsliste_shaper_origin.pdf)

Die Betriebsanweisung (`Betriebsanweisung_Shaper_Origin.tex`) ist standardmäßig aus. Zum Einschalten im `Makefile` die Zeile
`TARGET += Betriebsanweisung_Shaper_Origin` einkommentieren, dann wird sie als eigenes PDF und als Seite in der Einweisung gebaut.

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

[![Lizenz: CC BY-SA 3.0](https://licensebuttons.net/l/by-sa/3.0/de/88x31.png)</br>CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/)

Die Einweisung und die Betriebsanweisung (`betriebsanweisung/ba_shaper_origin.tex`, BA-SO-01) sind selbst
formuliert und enthalten keine Texte, Tabellen oder Abbildungen aus den Anleitungen von Shaper Tools oder
Festool. Die frühere Drehzahltabelle aus der Festool-Anleitung (`img/drehzahltabelle.pdf`) wurde durch eine
eigene Tabelle mit Richtwerten ersetzt. Alle Zeichnungen in `zeichnungen/` sind selbst mit TikZ erstellt;
Stil und Zeichnung zur Fräsrichtung stammen aus der
[Einweisung Oberfräse](https://github.com/fau-fablab/festool-oberfraese-einweisung) (ebenfalls CC BY-SA 3.0).
Symbole nur nach ISO 7010 aus `fablab-document`.

Für Details wird auf die Anleitungen von Shaper Tools verwiesen. **Beim Bearbeiten nichts aus den
Herstelleranleitungen übernehmen, auch nicht sinngemäß Satz für Satz.** Bilder bitte selbst zeichnen oder
fotografieren. Fotos aus dem Internet nur mit freier Lizenz (z.B. CC BY oder CC BY-SA) und mit Quellenangabe
in einer Datei `bilder/QUELLEN.md`.
