# Uni Passau Pandoc LaTeX Template

Latex Template für Hausarbeiten an der Universität Passau. Das Template folgt mehr oder weniger den [Vorgaben des Lehrstuhls für Politikwissenschaften](https://www.sobi.uni-passau.de/politikwissenschaft/studium-und-lehre/haus-und-abschlussarbeiten) und erfüllt größtenteils auch die Anforderungen des [Lehrstuhls für Soziologie](https://www.sobi.uni-passau.de/soziologie/studium-und-lehre/hinweise-zu-haus-und-abschlussarbeiten) (dem Titelblatt müssten evtl. ein paar Angaben hinzugefügt werden). Abweichungen gibt es bei der Schriftart, die aber in der metadata.yaml angepasst werden kann.

# How To

Um das Template zu nutzen, muss natürlich [Pandoc installiert](https://pandoc.org/installing.html) sein. Anschließend müssen nur die Metadaten angepasst werden, und schon kann mit dem Schreiben begonnen werden.

## Metadaten anpassen

Clone das Repository und passe die Angaben in der metadata.yaml an. Dort kannst du ein paar Änderungen an der Formatierung vornehmen, notwendig sind aber vor allem die Angaben zu Titel, Seminar, Autor etc.

## Quellenangaben und zitieren

Füge die Literatur im BibTeX- oder BibLaTeX-Format der bibliography.bib Datei hinzu (z.B. über einen Zotero export mit [Better BibTeX](https://github.com/retorquere/zotero-better-bibtex)). Alternativ können auch alle anderen von Pandoc [unterstützten Formate](https://pandoc.org/MANUAL.html#specifying-bibliographic-data) verwendet werden, dann muss allerdings noch der ```bibliography``` Eintrag in den Metadaten angepasst werden.

Anschließend können Literaturverweise im Text ganz einfach über die @citekey [Pandoc Citation Syntax](https://pandoc.org/chunkedhtml-demo/8.20-citation-syntax.html) hinzugefügt werden.

Standardmäßig wird APA 7 als Zitierstil genutzt, das kann aber leicht geändert werden. Einfach den gewünschten Stil im csl-Format herunterladen (beispielsweise im [Zotero Style Repository](https://www.zotero.org/styles)), im csl/ Ordner speichern und in der metadata.yaml Datei anpassen.

## Exportieren

Um die Markdown Datei als PDF zu exportieren, musst in der Kommandozeile der folgende Befehl innerhalb des Verzeichnisses ausgeführt werden:

```
pandoc Hausarbeit.md -d defaults.yaml -o Hausarbeit.pdf
```

Wenn die Arbeit mit Github synchronisiert wird, kann der PDF Export auch per Github Action bei jedem push automatisiert werden (dazu unten mehr).

# Einfacher Feedback-Prozess mit prose.io und GitHub Actions

coming soon