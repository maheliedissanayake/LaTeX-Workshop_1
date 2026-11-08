# LaTeX-Workshop anhand der Fickschen Gesetze

Materialien für einen 90-minütigen LaTeX-Workshop für Physikstudierende. Die Teilnehmenden setzen dabei selbst ein kleines Dokument: eine Zusammenfassung über die Fickschen Diffusionsgesetze. Darin stehen Abschnitte in eigenen Dateien, nummerierte Gleichungen, Abbildungen, eine Tabelle und ein Literaturverzeichnis. Der Text ist schon vorhanden, es geht nur ums Setzen. So passt der Workshop für Einsteiger*innen und für alle, die schon ein bisschen LaTeX können.

### Mahelie Dissanayake, 04.11.2026

## Inhalt

| Datei | Was ist das? |
|---|---|
| [`Presentation_Slides.pdf`](Presentation_Slides.pdf) | Präsentationsfolien: Grundlagen zu jedem Schritt, die fünf Aufgaben, typische Fehler und Quellen |
| [`Aufgabenblatt/`](Aufgabenblatt/) | Aufgabenblatt als PDF, als Word-Datei und als LaTeX-Quelltext |
| [`Spickzettel.pdf`](Spickzettel.pdf) | Zusammenfassung der wichtigsten Befehle |
| [`starter-projekt.zip`](starter-projekt.zip) | Starter-Projekt für die Teilnehmenden: Text und Kopfzeile fertig, Formatierung fehlt (siehe `TODO`-Kommentare) |
| [`Loesungen.pdf`](Loesungen.pdf) | Musterlösung als fertiges PDF |
| [`loesungen.zip`](loesungen.zip) | Musterlösung als LaTeX-Projekt zum Hochladen auf Overleaf |

## Ablauf

| Zeit | Thema |
|---|---|
| 0:00 | Einleitung |
| 0:05 | Schritt 1 · Grundgerüst |
| 0:20 | Schritt 2 · Struktur & Text |
| 0:36 | Schritt 3 · Formeln |
| 0:55 | Schritt 4 · Tabelle & Abbildung |
| 1:09 | Schritt 5 · Literatur & Verweise |
| 1:26 | Fehler, Ausblick, Fragen |

Vor jeder Aufgabe zeigen ein paar Folien das Nötige. Danach arbeiten alle selbst, insgesamt eine Stunde.

## Die Aufgabe

| Schritt | Darum geht's | Zeit |
|---|---|---|
| 1 · Grundgerüst | Dokumentklasse `scrartcl`, Pakete, Titel mit `\maketitle` auf eigener Titelseite | 11 min |
| 2 · Struktur & Text | Präambel und Abschnitte in eigene Dateien (`\input`), `\section`, Inhaltsverzeichnis auf eigener Seite, Listen | 12 min |
| 3 · Formeln | `equation` und `align`, eigene Befehle mit `\newcommand`, Verweise mit `\eqref` | 13 min |
| 4 · Abbildungen & Tabelle | `figure` mit `\includegraphics`, Tabellen mit `booktabs`, `\caption`, `\label`, `\ref`, `\FloatBarrier` | 11 min |
| 5 · Literatur & Querverweise | `biblatex` mit `\cite`, einen Eintrag selbst tippen, einen über Google Scholar holen, Literaturverzeichnis auf eigener Seite, klickbare Links mit `hyperref` | 13 min |

Jeder Schritt spielt sich hauptsächlich in einer Datei ab. Wer hängen bleibt, kann trotzdem mit dem nächsten Schritt weitermachen.

## Loslegen

**In Overleaf** (empfohlen, keine Installation nötig):

1. [`starter-projekt.zip`](starter-projekt.zip) herunterladen.
2. In [Overleaf](https://www.overleaf.com) auf **New Project → Upload Project** gehen und die ZIP-Datei hochladen.
3. Das Aufgabenblatt (`aufgaben.pdf`) liegt mit im Projekt. Einfach bei Schritt 1 anfangen.

**Lokal** (mit TeX Live oder MiKTeX):

1. `starter-projekt.zip` (für die Übung) oder `loesungen.zip` (Musterlösung) entpacken.
2. Im entpackten Ordner kompilieren:

```bash
latexmk -pdf main.tex
```

Im Starter-Projekt klappt das erst, wenn Schritt 1 erledigt ist. Vorher fehlt noch `\documentclass`.

`latexmk` startet auch `biber` für das Literaturverzeichnis. Gebraucht werden unter anderem KOMA-Script, `amsmath`, `siunitx`, `booktabs` und `biblatex`. Das alles ist in einer vollständigen TeX-Live-Installation enthalten.

## Quellen

Die inhaltlichen Aussagen auf den Folien (LaTeX-Grundlagen und Physik der Diffusion) sind mit Büchern und Fachartikeln belegt. Die Nummern unten rechts auf den Folien verweisen auf das Literaturverzeichnis auf der letzten Folie.

## Lizenz

[![CC BY 4.0](https://img.shields.io/badge/Lizenz-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/deed.de)

© 2026 Mahelie Dissanayake.

Das Material steht unter der Lizenz [Creative Commons Namensnennung 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/deed.de). Ihr dürft es frei nutzen, verändern und weitergeben, auch für eigene Workshops. Bedingung ist, dass ihr mich als Urheberin nennt, auf die Lizenz verweist und angebt, ob ihr etwas geändert habt. Den vollständigen Lizenztext findet ihr in [`LICENSE`](LICENSE).
