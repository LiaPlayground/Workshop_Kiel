<!--
author:   Sebastian Zug & André Dietrich

email:    @mail.org

version:  0.0.1

language: en

narrator: Deutsch Female

comment:  Try to write a short comment about
          your course, multiline is also okay.

-->

# Entwicklung von OER mit LiaScript und GitHub


**Allgemeine Ziele:**

* __100%__
  [Markdown](https://en.wikipedia.org/wiki/Markdown)-[Syntax](https://de.wikipedia.org/wiki/Syntax)
* __90%__
  [LiaScript](https://LiaScript.github.io)
* __20%__
  kennenlernen von [Versionmanagement](https://de.wikipedia.org/wiki/Versionsverwaltung) und kollaborativem Arbeiten mit [git](https://de.wikipedia.org/wiki/Git) und [GitHub](https://github.com)

---

**Zeitplan**

* __Vorstellung:__
  Infos zu uns, Forschungsziele, Projekte, etc.

* __Vorstellung/ Erwartungen der Teilnehmer__

  - Was erwarten Sie von der heutigen Veranstaltung, Welchen Hintergrund habe Sie?
  - Eintragung in ein Etherpad Dokument
  - Kurze Besprechung der Inhalte und der Arbeitsmethodik bei dessen Erstellung
  - synchrones kollaboratives Arbeiten --> Herausforderung Synchronisation

* __Motivation OER:__

  - Ziele, Zentrale Aussage zu den Anforderungen: Verteiltheit der Editierung
  - (Lösung mit Git), einfache Editierung interaktiver Inhalte (Lösung mit LiaScript)
  - Ableitung des folgenden Ablaufes - Phase 1: Github EInführung, Phase 2: LiaScript

* __Phase 1 - Einführung GitHub__

  - Mechanismen zur Synchronisation von Dokumenten, Abläufe in GitHub

* __Übung Github__

  - Alle Teilnehmer arbeiten an einer README.md Datei eines Projektes
  - Erklärung der Unterschiede zum Etherpad
  - Explizite Formatierung mit Markdown, Nachvollziehbarkeit der Veränderungen,
  - Einbettung in Entwicklungsumgebung


## Git & GitHub

Quellen:

- Pro Git book (2te Ausgabe) - _Ben Straub_
- online (deutsche Ausgabe): https://git-scm.com/book/de/v2


### Fachsprache & Fachchinesisch

     {{1}}
* ___git___

  - dezentrales Versionsmanagement System, entwickelt von [Linus Torvalds](https://de.wikipedia.org/wiki/Linus_Torvalds)
  - speichert die gesamte Historie eines Projektes
  - ermöglicht kooperatives Arbeiten mehrer Autoren
  - Download: https://git-scm.com/downloads

     {{2}}
* ___GitHub___

  - Platform für die Versionsverwaltung
  - Erweitert git um: __Reviews__, __Projekt-Management__, __Bug-Reports__, etc.
  - online: https://github.com
  - Wikipedia: https://de.wikipedia.org/wiki/GitHub

     {{3}}
* ___repository___ (___repo___)

  - das eigentliche Projekt
  - enthält alle Versionen und Entwicklungs-Zweige (branches)

     {{4}}
* ___fork^*^___

  - Kopie eines fremden ___Repositories___
  - Ziel: eigene Weiterentwicklung oder Zuarbeit

  ---

  <!-- style="max-width: 60rem" -->
  ``` ascii
  GitHub

  .----------------------.        fork        .---------------------.
  |                      |------------------->|                     |
  |   Main Repository    |                    | Personal Repository |
  |                      |<-------------------|                     |
  '----------------------'    pull request    '---------------------'
  ```

     {{5}}
* ___clone___

  - lokale Kopie eines ___Repositories___

  ---

  <!-- style="max-width: 60rem" -->
  ``` ascii
  GitHub

  .----------------------.        fork        .---------------------.
  |                      +------------------->|                     |
  |   Main Repository    |                    | Personal Repository |
  |                      |<-------------------+                     |
  '----------------------'    pull request    '--+------------------'
                                                 | clone          ^
  ---------------------------------------------- |           push |
  Local Machine                                  | pull           |
                                                 v                |
  .---------------------------------------------------------------+-.
  |                                                                 |
  |                            local files                          |
  |                                                                 |
  '-----------------------------------------------------------------'
  ```

     {{6}}
* ___pull___

  - Heruntladen/herunterziehen der Versionen aus einem entfernten ___repo___
  - (meist auf GitHub)

     {{7}}
* ___push___

  - Hochladen der lokalen Versionen zu einem entfernten ___repo___
  - (meinst auf GitHub)

     {{8}}
* ___pull request^*^___

  - Höfliche Anfrage der Übernahme von Änderungen

     {{9}}
* ___branch___

  - Verschiedene Entwicklungs-Zweige
  - Namensgebung: (beliebig aber ...)

    - `main`: Projekt (__Nur funktionierende Versionen__)
    - `develop`: Hauptentwicklungszweig
    - `test`: Test-Zweig für unsere Arbeit nicht nötig
    - `feat/Irgendwas`: kleine Erweiterungen


  <!-- style="max-width: 60rem" -->
  ``` ascii
  GitHub

  .----------------------.        fork        .---------------------.
  |                      +------------------->|                     |
  |   Main Repository    |                    | Personal Repository |
  |                      |<-------------------+                     |
  '----------------------'    pull request    '--+------------------'
                                                 | clone          ^
  ---------------------------------------------- |           push |
  Local Machine                                  | pull           |
                                                 v                |
  .---------------------------------------------------------------+-.
  |                                                                 |
  |  (main) *---*---*-----*----------------------------*-----*      |
  |              \       /                            /             |
  |  (develop)    o-----o--------o-----o--------o----o              |
  |                      \      /       \      /                    |
  |                       #----#         #----#                     |
  |                      (feat-1)       (feat-2)                    |
  '-----------------------------------------------------------------'
  ```

     {{10}}
* ___commit___

   - Hinzufügen einer neuen Version


     {{11}}
* ___checkout___

  - "auschecken" oder springen zu einem Zweiges oder einer Version

     {{12}}
* ___merge___

  - Übernehmen der Änderungen aus einem ___branch___ in einen anderen


### Verbinden von Atom und GitHub


## Teilen von Kursen via ...

**`https://LiaScript.github.io/course/?YOUR_COURSE_URL`**


    {{1}}
* [GitHub](https://github.com)
* [GitLab](https://gitlab.com)

    {{2}}
* [DropBox](https://DropBox.com)
* [nextCloud](https://nextCloud.com)

    {{3}}
* [Brave Browser](https://brave.com) via [IPFS](https://ipfs.io)
* [Beaker Browser](https://beakerbrowser.com) via [Hyper](https://hypercore-protocol.org)

  !?[Beaker-Browser demo](https://beakerbrowser.com/beaker-site-demo.mp4)<!-- autoplay="true" -->

* [Onion-Share](https://onionshare.org)

    {{4}}
* freier Webspace
* [CodiLia](https://github.com/liaScript/codilia)


## Markdown Tutorial

### Philosophy

> ~~__Markdown is intended to be as easy-to-read and easy-to-write as is feasible.__~~
>
> Readability, however, is emphasized above all else. A Markdown-formatted document ~~__should be publishable as-is__~~, as plain text, without looking like it’s been marked up with tags or formatting instructions. While Markdown’s syntax has been influenced by several existing text-to-HTML filters — including Setext, atx, Textile, reStructuredText, Grutatext, and EtText — the single ~~__biggest source of inspiration__~~ for Markdown’s syntax is the format of ~~__plain text email__~~.
>
>To this end, Markdown’s syntax is comprised entirely of punctuation characters, which ~~__punctuation characters have been carefully chosen so as to look like what they mean__~~. E.g., asterisks around a word actually look like \*emphasis\*. Markdown ~~__lists look like, well, lists__~~. Even ~~__blockquotes look like quoted passages of text__~~, assuming you’ve ever used email.
>
> -- by [John Gruber](https://daringfireball.net/projects/markdown/syntax#philosophy)

### Dialekte

### Grundlagen

> Blöcke werden "optisch" durch Leerzeilen voneinander getrennt

#### 1. Absätze und Formatierungen

#### 2. Listen

#### 3. Blockquotes

#### 4. Tabellen

#### 5. Verweise

#### 6. Bilder

#### 7. Trennlinien

#### 8. Code

#### 9. HTML

## LiaScript Tutorial

### Multimedia

Verweis -> !Bild --> ?Audio --> !?Video --> ??Unbekannt

#### Bilder und Texte


#### Formatierung

<!-- style="color: red; font-size: 4rem; max-width: 400px" -->
Blöcke<!-- style="background: green" --> und einzelne Elemente<!-- style="border: 3px dashed blue" --> können unterschiedlich formatiert werden!

> Merke: Kommentare __vor__ dem Block und __hinter__ dem Element.
>
> Siehe auch: [W3Schools](https://www.w3schools.com/Css/css_colors.asp)

##### Nützliche Stile

* Schriftfarbe:
  `color: red` oder `color: #FF0000` oder `color: rgb(1,0,0)`
* Schriftgröße:
  `font-size: 4rem` oder `font-size: 3cm` oder `font-size: 20px`
* Maximale Höhe & Breite:
  `max-height: 300px` `max-widht: 300px`
* Minimale Höhe & Breite:
  `min-height: 300px` `min-widht: 300px`
* Tatsächliche Höhe & Breite:
  `width: 300px` oder `width: 50%` oder `ẁidth: 50vw`
* Ränder:
  `border: 2px solid black` oder `border: 2px dashed black`
* Abstände:
  `padding: 3px` oder `padding-top: ..` oder `padding-left`
  oder `margin: 3px` oder `margin-top: ..` oder `margin-left`


#### Präsentationsformate

Buch/Präsentation/Folien

``` markdown
    --{{0}}--
Ich bin ein Kommentar, der laut vorgelesen werden kann.

    --{{1}}--
Es ist möglich, Kommentare mit Animation zu verbinden.

      {{1}}
?[audio](https://bigsoundbank.com/UPLOAD/mp3/1068.mp3)


    --{{2}}--
Blöcke können auch wieder verschwinden.

     {{2-3}}
| Tabellen |      sind      | cool  |
|:-------- |:--------------:|:----- |
| rechts   |   zentriert    | links |
| :-)      | $ f(x) = x^2 $ | <-->  |

liatab

    --{{3 Ukrainan Female}}--
Первоначально создан в 2004 году Джоном Грубером (англ. John Gruber) и Аароном
Шварцем.
Многие идеи языка были позаимствованы из существующих соглашений по
разметке текста в электронных письмах...


    {{3}}
Oder die Sprache kann geändert werden. Tippe "voice" um
eine Auswahl der unterstützen Sprachen zu erhalten
```

##### Inline Animationen

Hallo {2}{Welt, } dies ein Absatz mit internen Animationen {1-2}{**die auch wieder verschwinden können**}.

##### Sprachen Lernen `|>` oder `!>`

##### Versteckte Kommentare

    --{{1}}--
Dieser Text ist besonders wichtiges Zitat.

      {{1}}
> “Live as if you were to die tomorrow.
> Learn as if you were to live forever.”
>
> -- Mahatma Gandhi

<!-- --{{1}}--
Lebe so als ob du morgen sterben würdest.
Lerne so als ob du für immer Leben würdest.
Von Mahatma Ghandi.
-->

### Formeln

Nutzung von [KaTeX](https://katex.org)

Funktionsübersich: https://katex.org/docs/supported.html

1. Inline Formeln: `$ ... $` --> $ f(a,b,c) = (a^2+b^2+c^2)^3 $
2. Block Formeln: `$$ ... $$`

   $$
      \sum_{i=1}^\infty\frac{1}{n^2}
           =\frac{\pi^2}{6}
   $$

#### Interaktive Formeln
<!--
@formula: <script>console.html(`<lia-formula formula="@'input" displayMode="true"></lia-formula>`);"LIA: stop"</script>

-->

Zentriert nach `=`

``` latex
\begin{split}
  a &=b+c \\
    &=e+f \\
    &=g+h+i+j\\
a+b+&c+d=12\\
\end{split}
```
@formula

Hinzufügen einer Nummer

``` latex
\tag{33}
\begin{equation}
 a =b+c
\end{equation}
```
@formula

Definition einer Matrix und Nutzung von HTML.

``` latex
\begin{Bmatrix}
   a & b & c & d & e & f \\
   g & h & i & j & k & l \\
   m & n & o & p & q & r \\
   s & t & u & v & w & x \\
   y & z & ä & ö & ü &
   \htmlStyle{color: red; font-size: 26px}{ß}
\end{Bmatrix}
\\
\href{https://katex.org/docs/supported.html#html}{\KaTeX HTML support}
\\
\includegraphics[height=0.8em, totalheight=0.9em, width=0.9em, alt=KA logo]{https://katex.org/img/khan-academy.png}
```
@formula


### Quizzes

### Umfragen

### Aufgaben/Tasks

### Bemerkung zu Versionen



### Klassenräume

### Zeichnen mit ASCII-Art


                                    Multiline
    1.9 |    DOTS
        |                 ***
      y |               *     *
      - | r r r r r r r*r r r r*r r r r r r r
      a |             *         *
      x |            *           *
      i | B B B B B * B B B B B B * B B B B B
      s |         *                 *
        | *  * *                       * *  *
     -1 +------------------------------------
        0              x-axis               1


### Spaß mit Tabellen


### Erweiterungen

#### Wo finde ich Erweiterungen

#### Wie erstelle ich eigene Erweiterungen


## Export zu anderen Formaten
