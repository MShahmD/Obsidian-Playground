 **Bitte Source Modus einschalten, damit die Art des Schreibens von Markdown ersichtlich ist**
 Erstellt am 01.12.2022
 Author: Mohamad Shahm Damlakhi

# Obsidian Dokumentation
1. Index Seite für Obsidian (so eine Art Literaturverzeichnis)
   [Obsidian Index](https://help.obsidian.md/Obsidian/Index)
   2. How-To Liste für Obsidian 
   [Obsidian Format](https://help.obsidian.md/How+to/Format+your+notes)

# Allgemein 

## Headers
Es gibt wie bei HTML 6 unterschiedliche Headers-Stufen
\# Header 1
\## Header 2
\## Header 3
\#### Header 4
\##### Header 5
\###### Header 6

> [! Warning] - Headers sind hier ausgeschaltet
> In diesem Beispiel wurde absichtlich mit \  die Headers-Funktion gestört, damit die Ordnung des Dokuments nicht durcheinander kommt.
> Bei der Nutzung bitte dann "\" löschen, sonst funktioniert das nicht.

## Listen
Listen können so definiert werden:
### Ordered List
1.  Item 1
2.  Item 2
3.  Item 3
### Unordered List
- Item 1
- Item 2
- Item 3

## Tasklist
Um Tasklist zu erstellen, wird wie bei GitLab - [ ] genutzt
Beispiel:
- [x] Obsidian Dokumentation erstellen
- [x] Beispiele schreiben
- [x] Plugins installieren
- [ ] Git pushen
- [ ] Im Daily kurz zeigen

## Formatierung
- **Dieser Text wird fett gezeigt**
- *Dieser Text wird kursiv gezeigt*
- ~~Dieser Text wird durchgestrichen~~
- ==Dieser Text wird hervorgehoben==

## Hervorhebung
Es gibt bei Obsidian Blocke, die bestimmte Styles haben, um bestimmte Informationen hervorzuheben.

> [! Info]
> Hier sind Info

> [! Important]- Titel ist änderbar
> Hier steht ein wichtiger Hinweis
> Titel kann mit - geändert werden (s. oben)

> [! Done]
> Hier steht etwas, was fertig gemacht wurde

> [! FAQ]
> Hier steht Frage

> [! Warning]
> Hier steht eine Warnung

>[! ERROR]
>Hier steht Fehler

> [! BUG]
> Hier steht eine Klärung zu einem Bug

> [! Example]
> Hier steht ein Beispiel

> [! Quote]
> Hier steht eine Zitierung

## Verlinkung
- Mit \[\[ \]\] können andere Notizen verlinkt werden
 Z.B. [[Beispiel Notiz]]
- Mit \[\[Link |Alias name\]\] kann ein Alias vergeben werden.
 Z.B. [[Beispiel Notiz |My Alias]]

Verlinkung mit Kapitel/Abschnitt/Pargraph in einer Notiz:
1. Kaptiel [[Beispiel Notiz#Kapitel 1]]
2. Abschnitt [[Beispiel Notiz#Abschnitt 1]]
3. Pargraph: [[Beispiel Notiz#^d5d44e |Pargraph in Abschnitt 1]]
4. Tabelle: [[Beispiel Notiz#^Beispiel-Tabelle-ID]]

> [! Important]- ID können selbst definiert werden
> Bei Paragraphen können IDs selbst definiert werden.
> z.B. [[Beispiel Notiz#^My-ID]]

## URL Links
Mit \[Linkname\](www.domain.com)
z.B. [Link zu Obsidian HOW-TO](https://help.obsidian.md/How+to/Add+aliases+to+note)

## Tabellen
s. [[Playground#Advanced Table]]

## Dateien embedding
Mit \!\[\[Name der Datei\]\]  können Dateien embeddet werden.

- PDF Datei
  ![[Test.pdf]]
- Word Datei (über Drag und Drop)
  ![[Test.docx]]
- Bilder
   ![[Hello_World.jpeg]]

- Bilder Größe anpassen
![[Hello_World.jpeg | 500]]

> [! Warning] - Dateien müssen vorhanden sein
> Die Dateien müssen natürlich in Vault vorhanden sein. (bei unserem Vault unter Verzeichnis Dateien gespeichert)

> [! Danger] Bilder ersetzen 
> Wenn ein Bilder durch ein anderes Bilder mit demselben Namen ersetzt wurde, konnte Obsidian nicht erkennen.


## Text aus anderen Notizen importieren
- Beispiel bei einem Abschnitt
![[Beispiel Notiz#Abschnitt 1]]

- Beispiel bei einem Paragraph
![[Beispiel Notiz#^My-ID]]

- Beispiel bei einer Tabelle
![[Beispiel Notiz#^Beispiel-Tabelle-ID]]

> [! Warning] - Importieren von Tabellen
> Bei Tabellen muss vor ID und nach ID eine leere Zeile stehen, sonst wird die Tabelle nicht richtig dargestellt

## Code
- Für Inline Code werden einmalig Backticks `code` genutzt
Beispiel: `cd /obsidon/tutorial`

- Für Code Block werden Backticks \`\`\`Programmiersprache \`\`\` genutzt
Beispiele:

```bash
echo "Hello World"
ls
cd /obsidon/tutorial
```

```java
public static void main(String [] args) {
	System.out.println("Hello World");
}
```

```python
def test(parameter):
	print("Hello World")
```


## Formeln
Formeln können mit der Latex-Syntax eingefügt werden.
Es gibt inline-Formeln und Formeln in Zeilen.
- Für Ganzzeilige Formeln "\$\$"  wie klammern verwenden 
- inline-Formeln und Mathematische Symbole werden mit jeweils einem "\$" am Anfang und Ende eingeführt
Beispiel:
Self-Attention:
$K,Q,V$ werden aus gelernten Matrizen und der Multiplikation mit dem eingebetteten Eingabe Vektor $x_i$ des input embeddings erzeugt.
$$softmax(\frac{(KQ)}{\sqrt{d_k}})V$$
Es können viele weitere mathematische Symbole verwendet werden.
Eine kurze Übersicht ist unter dem Folgenden Link zu finden.
[Latex Cheat Sheet](http://tug.ctan.org/info/undergradmath/undergradmath.pdf)


## Toolbar Funktionen
### Gliederung
Oben rechts kann die Gliederung einer Notiz angeschaut werden. (s. Bild unten)

![[Gliederung-Symbol.png]]

### Todo-List/Checklist
Oben rechts kann die [[Playground#Todo-List/Checklist]] einer Notiz angeschaut werden. (s. Bild unten)

![[Todo.png]]

### Advanced Table
![[Advanced-Table.png]]

# Erweiterung mit Plugins

> [! Danger] Problem bei Änderung von Einstellungen 
> Da dieses Projekt in GitLab verwaltet wird, stehen alle unten beschriebenen Plugins zur Verfügung.
> Problematisch könnte es dann sein, wenn jemanden die Einstellungen für diese Plugins verändert.
> Deshalb bitte vor einer Änderung bei der Einstellung eines Plugins mit mir absprechen

## Kalender
Kalender Plugin öffnen und Tag auswählen, dann wird Notiz erstellt.
[Kalender Plugin](https://github.com/liamcain/obsidian-calendar-plugin)

## Checklist
Hashtag todo hinzufügen, dann kann alle Todos über Plugin angeschaut werden.

#todo
- [ ] First
- [ ] Hello World
- [ ] Third

> [! Warning]
> todo ist Standard-Einstellung

[Checklist Plugin](https://github.com/delashum/obsidian-checklist-plugin)

## Advanced Table
Mit Advanced Table plugin können Tabellen einfacher erzeugt werden.
Dafür muss mit | Überschrift1 | Überschrift 2| dann Neue-Zeile.
Dann wird die Tabelle  automatisch generiert.

Beispiel:
| Überschrift 1 | Überschrift 2 |
| ------------- | ------------- |
| Value 1       | Value 2       |

[Advanced Table Plugin](https://github.com/tgrosinger/advanced-tables-obsidian)

## Installieren von weiteren Plugins
Plugins können über Einstellung --> Externe Erweiterung --> Community Erweiterung --> Erweiterung aussuchen --> installieren