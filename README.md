# Fyndling TEI

Mittelalterliche Kochrezepte in TEI-P5, aus dem Bestand von
[fyndling.de](https://fyndling.de/rezepte/): historische Transkription, moderne
Übersetzung, Anmerkungen zu Lesarten und erschlossene Zutaten mit
Wikidata-Bezug.

**2404 Rezepte** aus **34 Kochbüchern**, dazu
34 Buchdateien mit den Quellenangaben.

Die Bücher sind unterschiedlich weit erschlossen - von einzelnen Rezepten
bis zum vollständigen Bestand. Die Tabelle unten nennt pro Buch, wie viele
es sind.

## Aufbau

```
tei/<rezept-id>.xml        ein Rezept
tei/books/<quelle>.xml     Buchebene: Handschrift, Edition, Lizenz
index.json                 maschinenlesbares Verzeichnis
```

Jede Datei trägt im `teiHeader` die Herkunft ihrer Transkription, die
Sprache des Originals und - wo vorhanden - den Bezug zum CoReMA-Korpus
(`<idno type="corema-sigle">`, `corema-object`, `corema-recipe`).

## Zutaten mit Normdaten

```xml
<ingredient en="pellitory" commodity="wikidata:Q828427" orig="perchtram">Bertram</ingredient>
```

Wo die Lesart nicht entschieden ist, stehen mehrere Kandidaten und
`cert="low"` - das ist eine Kandidatenliste, keine Identifikation:

```xml
<ingredient en="fat, unspecified" orig="vaists"
            commodity="wikidata:Q2789594 wikidata:Q1423543 wikidata:Q427457"
            cert="low">Schmalz</ingredient>
```

## Bücher

| Buch | Datierung | Rezepte | CoReMA |
|---|---|---:|---|
| Kochbuch des Meisters Hans | 1460 | 289 | [BS1](https://gams.uni-graz.at/o:corema.bs1) |
| Mondseer Kochbuch | 2. Hälfte 15. Jh. | 268 | [Gr1](https://gams.uni-graz.at/o:corema.gr1) |
| The Forme of Cury | ~1390 | 192 |  |
| Libro de Arte Coquinaria | ~1465 | 157 |  |
| Böhmisches Kochbuch - Kuchařství o rozličných krměch | 1535 | 134 |  |
| Ménagier de Paris | ~1393 | 114 |  |
| Koch und Kellermeisterei | 1574 | 110 |  |
| Berlin, Staatsbibliothek zu Berlin – Preußischer Kulturbesitz –, Handschriftenabteilung; Ms. germ. qu. 1187 | Mitte 15. Jh. | 106 | [B4](https://gams.uni-graz.at/o:corema.b4) |
| Wien, Österr. Nationalbibl., Cod. 2897 | Mitte 15. Jh. (Teil I) | 105 | [W1](https://gams.uni-graz.at/o:corema.w1) |
| Regensburger Kochbuch (Cgm 5919) | um 1500 | 104 | [M9](https://gams.uni-graz.at/o:corema.m9) |
| Das Buch von guter Speise | ~1350 | 101 | [M11](https://gams.uni-graz.at/o:corema.m11) |
| Münchner Kochbuchhandschriften (Cgm 384) | 2. Hälfte 15. Jh. | 83 | [M2](https://gams.uni-graz.at/o:corema.m2) |
| Reichenauer Kochbuch | 15. Jh. | 75 | [Ka1](https://gams.uni-graz.at/o:corema.ka1) |
| Registrum Coquine | ~1431-1435 | 70 |  |
| Haus- und Arzneibuch (Ka2) | 15. Jh. | 56 | [Ka2](https://gams.uni-graz.at/o:corema.ka2) |
| Klosterkochbuch Rott am Inn (Clm 15632) | 1458/1464 | 55 | [M10](https://gams.uni-graz.at/o:corema.m10) |
| Tegernseer Speisenbuch | 1453-1534 | 51 | [M13](https://gams.uni-graz.at/o:corema.m13) |
| Rheinfränkisches Kochbuch | ~1445 | 47 | [B1](https://gams.uni-graz.at/o:corema.b1) |
| Anonimo Toscano - Libro della cocina | Ende 14. Jh. | 40 |  |
| Königsberger Kochbuch | 15. Jh. | 34 | [B6](https://gams.uni-graz.at/o:corema.b6) |
| Weinbuch im Codex Donaueschingen | um 1500 (nach Ankenbrand zwischen 1484 und 1509) | 28 |  |
| Solothurner Küchenmeisterei | um 1487 | 26 | [So1](https://gams.uni-graz.at/o:corema.so1) |
| Alemannisches Büchlein von guter Speise (N1) | 1492 | 26 | [N1](https://gams.uni-graz.at/o:corema.n1) |
| Von guten und edlen Speisen (Wel ende edelike spijse) | ~1475 | 25 |  |
| Kogebog (Harpestreng-Handschrift NKS 66) | ~1300 | 25 |  |
| Kölner Küchenmeisterei | 2. Hälfte 15. Jh. oder 16. Jh. (umstritten) | 24 | [K1](https://gams.uni-graz.at/o:corema.k1) |
| Kochbuch Meister Eberhards | Mitte 15. Jh. | 23 | [A1](https://gams.uni-graz.at/o:corema.a1) |
| Le Viandier de Taillevent | ~1300 | 19 |  |
| Münchner Kochbuchhandschriften (Cgm 811) | 2. Viertel 15. Jh. | 4 | [M7](https://gams.uni-graz.at/o:corema.m7) |
| Münchner Kochbuchhandschriften (Cgm 725) | spätes 15. Jh. | 4 | [M5](https://gams.uni-graz.at/o:corema.m5) |
| Münchner Kochbuchhandschriften (Cgm 349) | 16. Jh. (Nachtrag) | 4 | [M1](https://gams.uni-graz.at/o:corema.m1) |
| Hausbuch aus Dietramszell (Cgm 467) | um 1477 | 3 | [M4](https://gams.uni-graz.at/o:corema.m4) |
| Nürnberg, Germanisches Nationalmuseum, Hs 3227a | um 1389 | 1 | [N2](https://gams.uni-graz.at/o:corema.n2) |
| Wolfenbüttel, Herzog-August-Bibliothek, Cod. Guelf. 42.3-5. Aug. 4° | 1543 | 1 | [Wo10](https://gams.uni-graz.at/o:corema.wo10) |

## Wie das Material entsteht - und was das bedeutet

**Ehrlich vorweg: hier arbeiten Sprachmodelle mit, und der Bestand ändert
sich laufend. Es gibt keine Gewähr.**

Der Weg eines Rezepts:

1. **Transkription** - von Dritten übernommen (siehe LICENSE), nicht von uns
   erstellt
2. **Übersetzung** - durch ein Sprachmodell, gegen historische Wörterbücher
   und den eigenen Korpus geprüft
3. **Preflight** - ein zweites Modell sucht Lesefallen, unbelegte
   Behauptungen und Zeilenumbruch-Artefakte
4. **Personas-Review** - mehrere Modelle prüfen dasselbe Rezept aus
   verschiedenen Blickwinkeln: Philologie, Küchenpraxis, Mediävistik,
   Korpus-Konsistenz, bei Getränken zusätzlich Önologie, bei Diätetik
   Medizingeschichte. Sie widersprechen einander, und der Widerspruch ist
   der Zweck.
5. **Redaktion** - ein Mensch entscheidet die strittigen Stellen

Nur Rezepte, die Schritt 5 durchlaufen haben, stehen in diesem Repositorium.

### Was den Unterschied macht: die Prüfinstanzen können nachschlagen

Der entscheidende Punkt an Schritt 3 und 4 ist nicht die Rollenverteilung,
sondern der **Werkzeugzugriff**. Die prüfenden Instanzen sind nicht auf ihr
Sprachmodellwissen zurückgeworfen - sie schlagen jedes strittige Wort in
historischen Wörterbüchern nach, lokal und online, und müssen ihre Lesart
mit einer Fundstelle belegen. Eine Lesart ohne Beleg ist im Verfahren eine
offene Frage, keine Übersetzung.

Genau das unterscheidet das Vorgehen von „mit KI übersetzt". Ohne
Nachschlagemöglichkeit hätte ein Modell zu `bersige`, `hawssen` oder
`zimendtrinttenn` eine plausible Meinung und keine Grundlage.

**24 Werke in 112 Dateien liegen lokal im Volltext** - mehrbändige und
alphabetisch geteilte Werke zählen dabei je Teil:

| Bereich | Werk |
|---|---|
| Mittelhochdeutsch | Benecke/Müller/Zarncke, Mittelhochdeutsches Wörterbuch (4 Bde.); Lexers Mittelhochdeutsches Handwörterbuch (3 Bde.) |
| Frühneuhochdeutsch | Götze, Frühneuhochdeutsches Glossar |
| Neuhochdeutsch | Grimm, Deutsches Wörterbuch (14 Bde.) |
| Mittellatein | Köbler, Mittellateinisches Wörterbuch (26 Teile) |
| Mittelniederdeutsch | Köbler, Mittelniederdeutsches Wörterbuch (26 Teile) |
| Altfranzösisch | Godefroy, Dictionnaire de l'ancienne langue française (10 Bde.) |
| Mittelniederländisch | Verdam, Middelnederlandsch Handwoordenboek (1911) |
| Mittelenglisch | Stratmann, Middle-English Dictionary (1891) |
| Alttschechisch | Gebauer, Slovník staročeský |
| Lateinische Glossare | Diefenbach, Glossarium latino-germanicum (1857) und Novum Glossarium (1867); Wülcker/Diefenbach (1885) |
| Dialekt-Idiotika | Schweizerisches Idiotikon (11 Bde.), Schmeller (bair.), Fischer (schwäb.), Frischbier (preuß., 2 Bde.), Autenrieth (pfälz.), Vilmar (kurhess.), Hübner (Salzburg 1796), Birlinger, Küchen- und Kellerdeutsch (1890) |
| Sachlexika | Heyne, Das deutsche Nahrungswesen (1901); Pritzel/Jessen, Die deutschen Volksnamen der Pflanzen (1882) |

**Dazu 53 Online-Nachschlagewerke**, überwiegend über das
[Wörterbuchnetz](https://woerterbuchnetz.de) der Universität Trier:
Mittelhochdeutsches Wörterbuch (MWB), Lexer, BMZ, Frühneuhochdeutsches
Wörterbuch (FWB), Deutsches Rechtswörterbuch (DRW), Mittellateinisches
Wörterbuch (MLW), Mittelniederdeutsches Wörterbuch (MNWB), Goethe-Wörterbuch,
Adelung, Campe, Krünitz, die regionalen Wörterbücher (Rheinisch, Pfälzisch,
Elsässisch, Lothringisch, Luxemburgisch, Schleswig-Holsteinisch,
Mecklenburgisch, Westfälisch u.a.), Wanders Deutsches Sprichwörter-Lexikon - sowie das
[Bayerische Wörterbuch (BDO)](https://bwb.badw.de) und das
[DWDS](https://www.dwds.de).

**Und drei projekteigene Nachschlagewerke:** die
[Mittelhochdeutsche Begriffsdatenbank](https://mhdbdb.plus.ac.at) als
Normdaten (Schreibvariante → Lemma → Bedeutungsfeld), das Referenzkorpus
Frühneuhochdeutsch (ReF, 1350-1650) für Belegdichte, und der eigene Korpus:
wie dieselbe Schreibung in anderen Handschriften gelesen wurde, mit
Belegzahl und Zeugen.

Alle Quellen sind über ein einheitliches Nachschlagewerkzeug erreichbar. Die
lokalen laufen bei jeder Abfrage mit; die Online-Wörterbücher werden auf
Anforderung nebenläufig abgefragt und danach zwischengespeichert, sodass die
zweite Suche nach demselben Wort ohne Netzzugriff auskommt.

### Was das für die Belastbarkeit heißt

- **Die Transkription ist die härteste Ebene.** Sie stammt aus
  wissenschaftlichen Editionen; Fehler dort sind Fehler der Edition.
- **Die Übersetzung ist eine Lesart, keine Wahrheit.** Wo mehrere möglich
  sind, steht das in den `<note type="gloss">`-Anmerkungen. Wo wir uns
  geirrt haben, korrigieren wir es - und die Korrekturhistorie zeigt, dass
  ein erheblicher Teil der Lesarten im Lauf der Zeit inhaltlich ersetzt
  wurde.
- **Zutaten-Normdaten sind Zuordnungen, keine Etiketten.** Ein
  Wikidata-Bezug ist unsere Deutung des Wortes an dieser Stelle. Wo wir
  unsicher sind, steht `cert="low"` mit mehreren Kandidaten - bitte nicht
  als Identifikation lesen.
- **Der Bestand ist nicht eingefroren.** Dateien ändern sich, wenn ein
  Rezept erneut geprüft wird. Wer einen festen Stand braucht, pinnt einen
  Commit.

Wer damit wissenschaftlich arbeitet: bitte gegen die Transkription prüfen
und die Anmerkungen mitlesen. Sie sind nicht Beiwerk, sondern der Ort, an
dem die Unsicherheit steht.

Fehler gefunden? Ein Issue hilft dem gesamten Korpus - solche Hinweise
fließen in die Prüfliste ein und werden auch an die Editionsprojekte
zurückgemeldet, aus denen die Transkriptionen stammen.

## Lizenz

**Zwei Ebenen, siehe LICENSE.** Kurz: die Transkriptionen stammen von
Dritten und stehen unter deren Lizenz mit Namensnennung; Übersetzung,
Anmerkungen und Zutatenerschließung sind unsere Arbeit unter
**CC BY-SA 4.0**. Die Herkunft steht pro Datei im `teiHeader`.

**Achtung, zwei Lizenzen.** 18 Rezepte aus dem Rheinfränkischen Kochbuch
stehen unter CC BY-**NC**-SA 4.0, sind also nicht kommerziell nutzbar. Alle
übrigen stehen unter CC BY-SA 4.0. Sie sind trotzdem alle enthalten - was
für welche Datei gilt, steht in der Datei selbst und ist maschinenlesbar:

```
teiHeader/fileDesc/publicationStmt/availability/licence/@target
```

Wer den Bestand kommerziell nutzen will, filtert darüber. Ein Skript, das
das Feld ignoriert und pauschal CC BY-SA annimmt, liegt bei diesen 18
Dateien falsch.

## Zitieren

Jedes Rezept hat eine stabile Adresse:

```
https://fyndling.de/rezepte/<id>/
https://fyndling.de/o:fyndling.<id>
```
Bevorzugt der persistente Bezeichner, er ueberlebt einen Umzug der Daten:

```
https://w3id.org/fyndling/<id>
```

Er handelt die Repraesentation aus: `Accept: text/html` fuehrt zur Seite,
`Accept: application/tei+xml` zur TEI-Datei.

Wo die Handschrift im CoReMA-Korpus erfasst ist, löst auch deren Kennung
auf: `https://fyndling.de/o:corema.<sigle>.<nr>`

## Erzeugung

Dieses Repositorium wird generiert, nicht von Hand gepflegt. Änderungen am
Inhalt gehören in den Fyndling-Bestand, nicht hierher - ein Pull Request
auf eine XML-Datei würde beim nächsten Export überschrieben. Fehler bitte
als Issue melden.
