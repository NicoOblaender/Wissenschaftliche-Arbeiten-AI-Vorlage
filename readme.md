# DHBW Mosbach LaTeX Template

Fork von [DHBW Heidenheim LaTeX Template](https://github.com/schnes4/dhbw-heidenheim-latex-template)
Angepasst für die DHBW Mosbach und den Studiengang Angewandte Informatik.

Zudem findet die Zitierung mit Fußnote statt.

**Inhalt:**

* [Templatestruktur](#templatestruktur)
* [Document Types](#document-types)
* [Komponenten einer Wissenschaftlichen Arbeit](#komponenten-einer-wissenschaftlichen-arbeit)
* [Contributors](#contributors)

## Templatestruktur

Das Template ist im Wesentlichen in 6 Teile unterteilt:

* main.tex
* ads/
* lang/
* settings/
* content/
* images/

### main.tex

main.tex ist die Kerndatei des Templates und damit auch die Datei, die kompiliert werden muss. Durch Importe anderer Dateien wird die Dokumentenstruktur beschrieben (kann bei Bedarf geändert werden wenn z.B. kein Sperrvermerk gewünscht wird).

### ads

Im Ordner ads befinden sich folgende vordefinierte Vorlagen, welche nicht angepasst werden müssen (Anpassungen erfolgen automatisch):

* Deckblatt
* Eigenständigkeitserklärung
* Sperrvermerk
* LaTeX Document Header

### lang

Im Ordner lang befinden sich alle notwendigen Übersetzungen.

### settings

Der Ordner settings beinhaltet zwei Dateien:

* main.tex
* document.tex

In der Datei main.tex sind grundlegende Einstellungen vordefiniert, welche nicht geändert werden müssen.

In der Datei document.tex müssen einige Angaben über die zu schreibende Arbeit gemacht werden:

| Variable            | Beschreibung                                           | Mögliche Werte                                                                                                                                                                                                       |
| ------------------- | ------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| documentLanguage    | Sprache der Arbeit                                     | de<br/> en                                                                                                                                                                                                           |
| documentType        | Art der Arbeit                                         | T1000 Projektarbeit (Semester 1 & 2) <br/> T2000 Projektarbeit (Semester 3 & 4) <br/> T3000 Projektarbeit (Semester 5 & 6) <br/> T3100 Studienarbeit (Semester 5 & 6) <br/> T3300 Bachelorarbeit                     |
| showCompanyLogo     | Ob das Firmenlogo auf dem Deckblatt gezeigt werden soll| true <br/> false                                                                                                                                                                                                     |
| showGenderNote      | Ob der Gender-Hinweis eingebunden werden soll          | true <br/> false                                                                                                                                                                                                     |
| showAppendix        | Ob der Anhang eingebunden werden soll                  | true <br/> false                                                                                                                                                                                                     |
| lofMinEntries       | Generierungs-Modus Abbildungsverzeichnis               | 0: Nie <br/> 1: Ab 1 Eintrag (Default) <br/> 2: Ab 3 Einträgen                                                                                                                                                       |
| lolMinEntries       | Generierungs-Modus Listings-Verzeichnis                | 0: Nie <br/> 1: Ab 1 Eintrag (Default) <br/> 2: Ab 3 Einträgen                                                                                                                                                       |
| lotMinEntries       | Generierungs-Modus Tabellenverzeichnis                 | 0: Nie <br/> 1: Ab 1 Eintrag (Default) <br/> 2: Ab 3 Einträgen                                                                                                                                                       |
| multipleAuthors     | Wurde die Arbeit von mehreren Autoren verfasst?        | true<br/> false                                                                                                                                                                                                      |
| documentAuthor      | Autor der Arbeit                                       |                                                                                                                                                                                                                      |
| documentTitle       | Titel der Arbeit                                       |                                                                                                                                                                                                                      |
| documentPeriod      | Dauer der Arbeit                                       |                                                                                                                                                                                                                      |
| matriculationNumber | Matrikelnummer des Autors                              |                                                                                                                                                                                                                      |
| locationUniversity  | Standort der DHBW                                      | Mosbach                                                                                                                                                                                                              |
| department          | Fakultät der DHBW in der sich der Autor befindet       |                                                                                                                                                                                                                      |
| course              | Kurs in dem sich der Autor befindet                    |                                                                                                                                                                                                                      |
| degree              | Abschluss, welcher mit dieser Arbeit angestrebt wird   | Bachelor of Science (INF2014-MI - INF2016-MI) <br/> Bachelor of Engineering (INF2014-IA/IM - INF2016-IA/IM) <br/> Bachelor of Science  (INF2017-IM/MI/IA)                                                            |
| lecture             | Vorlesung, für die die Arbeit geschrieben wurde        |                                                                                                                                                                                                                      |
| showLecture         | Ob die Vorlesung auf dem Deckblatt gezeigt werden soll | true <br/> false                                                                                                                                                                                                     |
| releaseDate         | Abgabedatum                                            |                                                                                                                                                                                                                      |
| releaseLocation     | Abgabeort                                              | Mosbach                                                                                                                                                                                                              |
| companyName         | Name des Unternehmens in dem der Autor angestellt ist  |                                                                                                                                                                                                                      |
| companyLocation     | Firmensitz                                             |                                                                                                                                                                                                                      |
| tutor               | Betrieblicher Betreuer der Arbeit                      |                                                                                                                                                                                                                      |
| evaluator           | Zweitkorrektor der Arbeit                              |                                                                                                                                                                                                                      |
| linkColor           | Farbe von Verlinkungen                                 | 000000 (schwarz)                                                                                                                                                                                                     |

### content

### images

# Document Types

Das Template bietet die folgenden verschiedenen Document Types an:

* T1000 Project Thesis (Praxissemester 1 & 2)
* T2000 Project Thesis (Praxissemester 3 & 4)
* T3000 Project Thesis (Praxissemester 5 & 6)
* T3100 Seminar Paper (Semester 5 & 6)
* T3300 Bachelor Thesis
* Sonstige

Das Template passt alle relevanten Einstellungen automatisch an, sobald der Document Type geändert wird.

## Document Type spezifische Besonderheiten

### T1000 & T3000 (Projektarbeiten)

Bei diesen Projektarbeiten wird die Arbeit primär vom betrieblichen Betreuer (Tutor) bewertet. Das Feld für den DHBW-Gutachter (Evaluator) wird daher auf dem Deckblatt automatisch ausgeblendet. (Die T2000 bildet eine Ausnahme, hier werden beide Gutachter angezeigt).

### T3100 (Studienarbeit / Seminar Paper)

Die Studienarbeit ist eine reine Hochschularbeit. Aus diesem Grund werden das Unternehmenslogo, die Nennung der Firma sowie der betriebliche Betreuer auf dem Deckblatt automatisch ausgeblendet. Ebenso entfällt der Sperrvermerk komplett. Der Bearbeitungszeitraum wird auf dem Deckblatt automatisch auf "2 Semester" gesetzt. Des Weiteren ist es möglich, die Studienarbeit als Gruppe abzugeben. Hierfür gibt es die Variable `multipleAuthors`. Ist diese auf `true` gesetzt, passt sich die Eigenständigkeitserklärung selbst von der Ich- zur Wir-Form an. Mehrere Autoren sind lediglich mit Komma getrennt in die Variable `documentAuthor` einzutragen.

### Sonstige

Für andere als die vordefinierten Types kann der Dokumenttyp (z.B. Hausarbeit) auch als individueller Text direkt in das Feld `documentType` eingetragen werden. Dieser Text wird dann auf dem Deckblatt ausgegeben. Es greifen in diesem Fall allerdings keine bedingten Formatierungen oder Ausblendungen (wie z.B. das automatische Ausblenden des Unternehmens bei einer Studienarbeit), sondern es wird der Standardumfang der Vorlage gerendert.

# Komponenten einer Wissenschaftlichen Arbeit

## Abstract

An abstract is a brief summary of a research article, thesis, review, conference proceeding or any in-depth analysis of a particular subject or discipline, and is often used to help the reader quickly ascertain the paper's purpose. When used, an abstract always appears at the beginning of a manuscript, acting as the point-of-entry for any given scientific paper or patent application. Abstracting and indexing services for various academic disciplines are aimed at compiling a body of literature for that particular subject.

The terms précis or synopsis are used in some publications to refer to the same thing that other publications might call an ``abstract''. In``management'' reports, an executive summary usually contains more information (and often more sensitive information) than the abstract does.

Quelle: <http://en.wikipedia.org/wiki/Abstract_(summary>)

## Glossar und Abkürzungen (Glossaries & Acronyms)

Die Vorlage verwendet das leistungsstarke Paket `glossaries`, um sowohl Abkürzungen als auch Glossareinträge zentral zu verwalten. 

### Einfache Glossareinträge und Abkürzungen

Du kannst Standard-Glossareinträge oder einfache Abkürzungen in der Datei `content/glossary.tex` definieren:
* `\newglossaryentry{label}{name={Begriff}, description={Erklärung}}`
* `\newacronym{label}{Abk.}{Ausgeschriebene Form}`

### Verknüpfte Abkürzungen mit Glossareintrag

Oft möchte man eine Abkürzung im Text verwenden, aber diese gleichzeitig im Glossar ausführlich erklären lassen. Dafür stellt die Vorlage den Befehl `\newglossarywacronym` zur Verfügung.

**Verwendung:**
`\newglossarywacronym[Alternativer Text für erste Nennung]{Label}{Ausgeschriebene Form}{Ausführliche Beschreibung}`

**Beispiel:**
```LaTeX
\newglossarywacronym{API}{Application Programming Interface}{Eine API ist eine Programmierschnittstelle...}
\newglossarywacronym[User Interface (englisch für Benutzeroberfläche)]{UI}{User Interface}{Ein UI ist die Benutzeroberfläche...}
```

**Verwendung im Text:**
Mit dem Befehl `\gls{Label}` referenzierst du den Eintrag im Text. 
* Beim **ersten Aufruf** wird standardmäßig die Langform und dahinter die Abkürzung gedruckt: *Application Programming Interface (API)*. Wurde jedoch der optionale Zusatz angegeben, ersetzt dieser die Langform komplett: *User Interface (englisch für Benutzeroberfläche) (UI)*
* Bei **allen weiteren Aufrufen** wird nur noch die Kurzform (Abkürzung) gedruckt: *API* bzw. *UI*

Darüber hinaus erzeugt dieser Befehl automatisch einen Querverweis, der die Abkürzung sauber mit dem ausführlichen Glossareintrag verlinkt.

Weitere Befehle für den Text:
* `\gls{Label}`   --> Standardaufruf (schreibt beim ersten Mal Lang+Kurz, danach Kurz)
* `\glspl{Label}` --> Plural (hängt ein "s" an)
* `\glsdisp{Label}{Eigener Text}` --> Verlinkt auf das Label, zeigt aber deinen eigenen Text an.

## Appendix

(Beispielhafter Anhang)

```LaTeX
{\Large
\begin{enumerate}[label=\Alph*.]
 \item Assignment 
 \item List of CD Contents
 \item CD 
\end{enumerate}
}
\pagebreak
%\includepdf[pages=-,scale=.9,pagecommand={}]{Aufgabenstellung.pdf} % PDF um 10% verkleinert einbinden --> Kopf- und Fußzeile  werden so korrekt dargestellt. Die Option `pages' ermöglicht es, eine bestimmte Sequenz von Seiten (z.B. 2-10 oder `-' für alle Seiten) auszuwählen.
\pagebreak
\section*{B. Auflistung der Begleitmaterial-Archivdatei }
Die Archivdatei wurde zusammen mit der Online-Version dieser Ausarbeitung auf die Lernplattform hochgeladen.
\begin{tabbing}
 mm \= mm \= mmmmmmmmmmmmmmmm \= \kill
 $\vdash$ \textbf{Literature/} \\ 
 | \> $\vdash$ \textbf{Citavi-Project(incl pdfs)/} \> \> $\Rightarrow$ \textit{Citavi (bibliography software) project with}\\
 | \> | \> \> \textit{almost all found sources relating to this report.} \\
 | \> | \> \> \textit{The PDFs linked to bibliography items therein} \\
 | \> | \> \> \textit{are in the sub-directory `CitaviFiles'}\\
 | \> | \>  -- bibliography.bib  \> $\Rightarrow$ \textit{Exported Bibliography file with all sources}\\
 | \> | \>  -- Studienarbeit.ctv4  \>  $\Rightarrow$ \textit{Citavi Project file}\\
 | \> | \>  $\vdash$ \textbf{CitaviCovers/} \>  $\Rightarrow$ \textit{Images of bibliography cover pages}\\
 | \> | \>  $\vdash$ \textbf{CitaviFiles/} \> $\Rightarrow$ \textit{Cited and most other found PDF resources}\\ %\llcorner
 | \> $\vdash$ \textbf{eBooks/} \\
 | \> $\vdash$ \textbf{JournalArticles/} \\
 | \> $\vdash$ \textbf{Standards/}\\
 | \> $\vdash$ \textbf{Websites/} \\ %\llcorner
 |\\
 $\vdash$ \textbf{Presentation/} \\
 | \>  --presentation.pptx\\
 | \>  --presentation.pdf\\
 |\\
 $\vdash$ \textbf{Report/} \\ %\llcorner
 \>  -- Aufgabenstellung.pdf\\
 \>  -- Studienarbeit2.pdf\\
 \>  $\vdash$ \textbf{Latex-Files/}   $\Rightarrow$ \textit{editable \LaTeX~files and other included files for this report}\\ %\llcorner
 \> \>  $\vdash$  \textbf{ads/}    \> $\Rightarrow$ \textit{Front- and Backmatter}\\
 \> \>  $\vdash$  \textbf{content/}  \> $\Rightarrow$ \textit{Main part}\\
 \> \>  $\vdash$  \textbf{images/}   \> $\Rightarrow$ \textit{All used images}\\
 \> \>  $\vdash$  \textbf{lang/}  \> $\Rightarrow$ \textit{Language files for \LaTeX~template}\\ %\llcorner
\end{tabbing}
```

## Contributors

* Tobias Dreher
* Yves Fischer
* Michael Gruben
* Markus Barthel
* Prof. Dr. Rolf Assfalg
* Stefan Schneider
* Andreas Kießling
* Sarah Willibald
