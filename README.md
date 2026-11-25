# Fyndling TEI

Mittelalterliche Kochrezepte in TEI-P5, aus dem Bestand von
[fyndling.de](https://fyndling.de/rezepte/): historische Transkription, moderne
Übersetzung, Anmerkungen zu Lesarten und erschlossene Zutaten mit
Wikidata-Bezug.

**9442 Rezepte** aus **62 Rezeptsammlungen**, dazu
62 Dateien auf Sammlungsebene mit den Quellenangaben.

Die Sammlungen sind überwiegend handschriftlich überliefert; einige der
späteren sind Drucke. „Buch" wäre für die Handschriften falsch: gedruckt
wurde erst ab 1485 (Küchenmeisterei), alles Ältere sind Lagen aus Papier
oder Pergament. Wir sagen deshalb Sammlung, wo es um den Text geht, und
Handschrift oder Druck, wo der Gegenstand gemeint ist. Dank an Helmut W.
Klug für die Präzisierung.

Die Sammlungen sind unterschiedlich weit erschlossen - von einzelnen Rezepten
bis zum vollständigen Bestand. Die Tabelle unten nennt pro Sammlung, wie viele
es sind.

## Aufbau

```
tei/<rezept-id>.xml        ein Rezept
tei/books/<quelle>.xml     Sammlungsebene: Handschrift bzw. Druck, Edition, Lizenz
index.json                 maschinenlesbares Verzeichnis
offene-lesarten.json       alle ungeklärten Wörter und Lesungen, mit Blatt und Alternativen
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

| Sammlung | Datierung | Rezepte | CoReMA |
|---|---|---:|---|
| Ein new Kochbuch | 1581 | 2028 |  |
| Kunstbuch von mancherley Essen | 1598 | 1362 |  |
| Churer Kochbuch (Staatsarchiv Graubünden, NH.2) | 1559 (Grundstock; Nachträge bis ins späte 17. Jh.) | 523 |  |
| Ein köstlich new Kochbuch | 1598 | 483 |  |
| Das Kochbuch des Balthasar Staindl | 1545 | 294 |  |
| Kochbuch des Meisters Hans | 1460 | 289 | [BS1](https://gams.uni-graz.at/o:corema.bs1) |
| Ménagier de Paris | ~1393 | 289 |  |
| Berlin, Staatsbibliothek zu Berlin – Preußischer Kulturbesitz –, Handschriftenabteilung; Ms. germ. qu. 1187 | Mitte 15. Jh. | 269 | [B4](https://gams.uni-graz.at/o:corema.b4) |
| Wien, Österr. Nationalbibl., Cod. 2897 | Mitte 15. Jh. (Teil I) | 269 | [W1](https://gams.uni-graz.at/o:corema.w1) |
| Mondseer Kochbuch | 2. Hälfte 15. Jh. | 268 | [Gr1](https://gams.uni-graz.at/o:corema.gr1) |
| Das Kochbuch der Philippine Welser | 1543-44 | 242 |  |
| Libro de Arte Coquinaria | ~1465 | 225 |  |
| Das Kochbuch der Sabina Welserin | 1553 | 206 |  |
| The Forme of Cury | ~1390 | 192 |  |
| Kölner Küchenmeisterei | 2. Hälfte 15. Jh. oder 16. Jh. (umstritten) | 182 | [K1](https://gams.uni-graz.at/o:corema.k1) |
| Solothurner Küchenmeisterei | um 1487 | 152 | [So1](https://gams.uni-graz.at/o:corema.so1) |
| Rasch: Weinbuch | um 1580 | 147 |  |
| Das Kochbuch der Maria Stenglerin | 1554 | 145 |  |
| Böhmisches Kochbuch - Kuchařství o rozličných krměch | 1535 | 144 |  |
| Rezeptbuch der Sarah Longe | 17. Jh., Nachträge bis 18. Jh. | 141 |  |
| Wolfenbüttel, Herzog-August-Bibliothek, Cod. Guelf. 42.3-5. Aug. 4° | 1543 | 116 | [Wo10](https://gams.uni-graz.at/o:corema.wo10) |
| Koch und Kellermeisterei | 1574 | 110 |  |
| Das geöffnete Kabinett des Sir Kenelm Digby | 1669 | 105 |  |
| Regensburger Kochbuch (Cgm 5919) | um 1500 | 104 | [M9](https://gams.uni-graz.at/o:corema.m9) |
| Reichenauer Kochbuch | 15. Jh. | 104 | [Ka1](https://gams.uni-graz.at/o:corema.ka1) |
| Das Buch von guter Speise | ~1350 | 101 | [M11](https://gams.uni-graz.at/o:corema.m11) |
| Münchner Kochbuchhandschriften (Cgm 384) | 2. Hälfte 15. Jh. | 83 | [M2](https://gams.uni-graz.at/o:corema.m2) |
| Registrum Coquine | ~1431-1435 | 70 |  |
| Rheinfränkisches Kochbuch | ~1445 | 61 | [B1](https://gams.uni-graz.at/o:corema.b1) |
| Von guten und edlen Speisen (Wel ende edelike spijse) | ~1475 | 60 |  |
| Haus- und Arzneibuch (Ka2) | 15. Jh. | 56 | [Ka2](https://gams.uni-graz.at/o:corema.ka2) |
| Klosterkochbuch Rott am Inn (Clm 15632) | 1458/1464 | 55 | [M10](https://gams.uni-graz.at/o:corema.m10) |
| Tegernseer Speisenbuch | 1453-1534 | 51 | [M13](https://gams.uni-graz.at/o:corema.m13) |
| Ryff: Confect oder Latwergen büchlin | 1562 | 50 |  |
| Le Viandier de Taillevent | ~1300 | 49 |  |
| Clutius: Von den Bienen (Buch 3: Vom Honig) | 1597 | 44 |  |
| Anonimo Toscano - Libro della cocina | Ende 14. Jh. | 40 |  |
| Königsberger Kochbuch | 15. Jh. | 34 | [B6](https://gams.uni-graz.at/o:corema.b6) |
| Worlidge: Britischer Weingarten (Getränke) | 1676 | 33 |  |
| Weinbuch im Codex Donaueschingen | um 1500 (nach Ankenbrand zwischen 1484 und 1509) | 28 |  |
| Alemannisches Büchlein von guter Speise (N1) | 1492-1494 | 26 | [N1](https://gams.uni-graz.at/o:corema.n1) |
| Kogebog (Harpestreng-Handschrift NKS 66) | ~1300 | 25 |  |
| Kochbuch Meister Eberhards | Mitte 15. Jh. | 23 | [A1](https://gams.uni-graz.at/o:corema.a1) |
| Royer: Gartengewächse in der Küche | 1648 | 20 |  |
| Butler: Die weibliche Monarchie (Met, Honig, Wachs) | 1623 | 18 |  |
| Woolley: Das königliche Kabinett (Getränke) | 1670 | 17 |  |
| Nürnberg, Germanisches Nationalmuseum, Hs 3227a | um 1389 | 15 | [N2](https://gams.uni-graz.at/o:corema.n2) |
| Wellcome MS.550: medizinische Sammelhandschrift, Abschnitt „de potibus“ (Getränke) | frühes 15. Jh. | 14 |  |
| Salzburg, Cod. M III 3 („Speyerer Kompendium“): Lautertränke und Bierbrauen | um 1460 | 13 |  |
| Münchner Kochbuchhandschriften (Cgm 725) | spätes 15. Jh. | 13 | [M5](https://gams.uni-graz.at/o:corema.m5) |
| Michaelbeurer Kochbuch (Man. cart. 81) | 15. Jh. (Sammelhandschrift, datierte Teile 1444 und 1451) | 12 | [Mi1](https://gams.uni-graz.at/o:corema.mi1) |
| Wellcome MS.144: Rezeptbuch (sechs Metrezepte) | um 1650 bis 1731 | 6 |  |
| Glauber: Reicher Schatz- und Sammelkasten, Zweite Centuria (Gefrierkonzentration) | 1660 | 6 |  |
| Hohberg: Georgica Curiosa (Vom Met-Sieden) | 1682 | 5 |  |
| Wirsung: Arzneibuch (Met und Honiggetränke) | 1568 | 5 |  |
| Münchner Kochbuchhandschriften (Cgm 811) | 2. Viertel 15. Jh. | 4 | [M7](https://gams.uni-graz.at/o:corema.m7) |
| Münchner Kochbuchhandschriften (Cgm 349) | 16. Jh. (Nachtrag) | 4 | [M1](https://gams.uni-graz.at/o:corema.m1) |
| Arzneibuch Wellcome MS.MSL.136 (Met und Honiggetränke) | Mitte 15. Jh. | 4 |  |
| Hausbuch aus Dietramszell (Cgm 467) | um 1477 | 3 | [M4](https://gams.uni-graz.at/o:corema.m4) |
| Hermann: Der livländische Landmann (Met) | 1695 | 2 |  |
| Haus- und Arzneibuch im Codex Donaueschingen 792 | um 1450/1452 (Hoffmann/Sturm 2025) | 2 |  |
| Syreniusz: Kräuterbuch (Gerstenmet) | 1613 | 1 |  |

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

**Lokal im Volltext liegen rund 150 Wörterbücher und Glossare (564 Dateien)
und Sachquellen in 275 Dateien** (Stand 2026-11-17). Zeichen in den Tabellen:
⬇ = von uns neu gelesen oder in der OCR repariert und auf
[fyndling.de/woerterbuecher.html](https://fyndling.de/woerterbuecher.html)
frei herunterladbar; *intern* = urheberrechtlich geschützt, wir schlagen
darin nach und zitieren mit Fundstelle, geben den Volltext aber nicht
weiter. Alles andere ist gemeinfreie Fremd-OCR (meist archive.org, BSB).

| Bereich | Wörterbücher und Glossare |
|---|---|
| Mittel- und Frühneuhochdeutsch | Benecke/Müller/Zarncke, Mhd. Wörterbuch (1854-66); Lexer, Mhd. Handwörterbuch (1872-78) mit Nachträgen; Pfeiffer, Wörterbuch zu Megenbergs Buch der Natur (1861) ⬇; Götze, Fnhd. Glossar (1920); Wülcker/Diefenbach, Hoch- und niederdeutsches Wörterbuch (1885); Haltaus, Glossarium Germanicum (1758) ⬇; Scherz/Oberlin, Glossarium Germanicum (1781-84) ⬇ |
| Glossare zu Chroniken und Urkunden | Lexer, Augsburger (1865/66) ⬇ und Nürnberger Chroniken (1874) ⬇; Birlinger, Kölner Chroniken (1875/77) ⬇; Basler Chroniken (1890/1902); Groote, Wierstraats Reimchronik Neuss (1855) ⬇; Hampe, Nürnberger Ratsverlässe (1904) ⬇; Brucker/Wethly, Straßburger Zunftverordnungen (1889); Hashagen, Kölner Zunfturkunden (1907, *intern*); Tomaschek, Salzburger Taidinge (1870) ⬇; Egger, Tiroler Weistümer (1891) ⬇ |
| Frühneuzeitliche Wörterbücher und Nomenklatoren | Vocabularius Ex quo (Köln um 1475) ⬇; Teuthonista (Köln 1477) ⬇; Dasypodius, Nomenclatura (1536) ⬇; Frisius, Nomenclator (1556, Speisen und Getränke) ⬇; Maaler, Die Teütsch spraach (1561) ⬇; Golius, Onomasticon (1579) ⬇; Frischlin, Nomenclator trilinguis (1586) ⬇; Emmel, Nomenclator quadrilinguis (1592) ⬇; Chytraeus, Nomenclator Latinosaxonicus (1601) ⬇; Henisch, Teutsche Sprach und Weißheit (1616) ⬇; Schottelius, Haubtsprache (1663) ⬇; Stieler, Stammbaum und Fortwachs (1691) ⬇; Frisch, Teutsch-Lateinisches Wörter-Buch (1741) ⬇ |
| Neuhochdeutsch | Grimm, Deutsches Wörterbuch (1854-1961, A-Z); Kaltschmidt, Gesammt-Wörterbuch (1854) |
| Mittellatein | Köbler, Mittellateinisches Wörterbuch; Diefenbach, Glossarium latino-germanicum (1857) ⬇, Novum Glossarium (1867) ⬇ und lateinisch-deutsch-böhmisches Wörterbuch (1846) ⬇ |
| Oberdeutsche Mundarten | Schmeller, Bayerisches Wörterbuch (1872-77) ⬇; Schweizerisches Idiotikon (1881 ff., Bd. 1-13, Bd. 12-13 *intern*); Stalder, Schweizerisches Idiotikon (1806/12) ⬇; Schmidt/Tobler, Idioticon Bernense (1855-57) ⬇; Spreng, Idioticon Rauracum (1887) ⬇; Seiler, Basler Mundart (1879); Fischer, Schwäbisches Wörterbuch (1904-36, Bd. 3-6 ⬇); Schmid, Schwäbisches Wörterbuch (1831, 1844); Birlinger, Schwäbisch-Augsburgisches Wörterbuch (1864); Martin/Lienhart, Elsässisches Wörterbuch (1899-1907) ⬇; Schmidt, Historisches Wörterbuch der elsässischen Mundart (1901) ⬇; Autenrieth, Pfälzisches Idiotikon (1899) ⬇; Höfer, Oberdeutsche Mundart (1815) ⬇; Castelli, Österreich unter der Enns (1847) ⬇; Unger/Khull, Steirischer Wortschatz (1903) ⬇; Lexer, Kärntisches Wörterbuch (1862) ⬇; Schöpf, Tirolisches Idiotikon (1866) ⬇; Hübner, Salzburger Idiotikon (1796); Schröer, Ungrisches Bergland (1858) ⬇; Meisinger, Rappenauer Mundart (1906) ⬇; Ruckert, Unterfränkische Mundart (1901/02) ⬇; Maas, Das Willsche Idiotikon (Nürnberg, 1959, *intern*) |
| Mittel- und ostdeutsche Mundarten | Vilmar, Kurhessen (1868) ⬇; Crecelius, Oberhessisch (1897/99) ⬇; Kehrein, Nassau (1891) ⬇; Schön, Saarbrücker Land (1922) ⬇; Reinwald, Hennebergisch (1793/1801) ⬇; Müller-Fraureuth, Obersächsisch (1911/14) ⬇; Weinhold, Schlesisch (1855) ⬇; Knothe, Schlesisch in Nordböhmen (1888) ⬇; Frischbier, Preußisch (1882/83); Hupel, Lief- und Ehstland (1795) ⬇ |
| Niederdeutsch | Köbler, Mittelniederdeutsches Wörterbuch; Schiller/Lübben, Mittelniederdeutsches Wörterbuch (1875-81); Bremisch-niedersächsisches Wörterbuch (1767-71, 1869) ⬇; Schambach, Göttingen-Grubenhagen (1858) ⬇; Strodtmann, Idioticon Osnabrugense (1756) ⬇; Woeste, Westfälisch (1882) ⬇; Dähnert, Pommersch-rügisch (1781) ⬇; Danneil, Altmärkisch (1859) |
| Mittelniederländisch | Verwijs/Verdam, Middelnederlandsch Woordenboek (1885-1941, mit Beekmans Aanvullingen) ⬇; Verdam, Handwoordenboek (1911) mit Supplement (1983, *intern*); Kiliaan, Etymologicum (1599); Braekman, Botanisch glossarium (1965), Geneeskundige recepten (1970) und Medische en technische recepten (1975), alle *intern*; Vandewalle, Oude maten (1984, *intern*) |
| Englisch | Stratmann/Bradley, Middle-English Dictionary (1891); Halliwell, Archaic and Provincial Words (1846/47); Baret, Alvearie (1574); Florio, Queen Anna's New World of Words (1611); Blount, Glossographia (1656); Phillips, New World of English Words (1658); Blankaart, Physical Dictionary (1684); Holme, Academy of Armory (1688, Auszug); Ludwig, English-German-French (1706) ⬇; Macdonell, Glossar zu Digby (1910) |
| Französisch | Godefroy, Ancienne langue française (1880-1902); Huguet, Langue française du seizième siècle (1925-67); Nicot, Thresor (1606) ⬇; Cotgrave, French and English (1611) ⬇; Furetière, Dictionnaire universel (1690) ⬇; Corneille, Arts et sciences (1694) ⬇; Lémery, Drogues simples (1698); Chomel, Dictionnaire oeconomique (1709) ⬇; Doursther, Poids et mesures (1840) |
| Italienisch, Spanisch | Boerio, Veneziano (1829); D'Ambra, Napolitano (1873); Covarrubias, Tesoro de la lengua castellana (1611) ⬇ |
| Nordisch, Slawisch | Söderwall, Fornsvensk ordbok (1884-1918, Supplement 1925-73; Språkbanken, CC BY 4.0) mit Formenlexikon; Gebauer, Slovník staročeský (Bd. 1, 1903); Jungmann, Slownjk (1835-39); Kott, Česko-německý slovník (1878-1906); Knapski, Thesaurus (1643) ⬇; Linde, Słownik (1807-14) ⬇ |
| Pflanzen, Tiere, Arznei | Pritzel/Jessen, Volksnamen der Pflanzen (1882) ⬇; Lonitzer, Naturalis historiae tomus II (1555) ⬇; Bauhin, Pinax (1623) ⬇; Gerard/Johnson, Herball (1633); Earle, English Plant Names (1880) ⬇; Mowat, Sinonoma Bartholomei (1882) ⬇ und Alphita (1887) ⬇; Britten/Holland, English Plant-Names (1886); Heukels, Volksnamen van planten (1907); Durheim, Schweizerisches Pflanzen-Idiotikon (1856) ⬇; Leroy, Pomologie (1867-79); Dorn, Dictionarium Paracelsi (1584) ⬇; Ruland, Lexicon alchemiae (1612); Sommerhoff, Lexicon pharmaceutico-chymicum (1701); Gessner, Vogelbuch (1557) ⬇, Thierbuch und Fischbuch (1563) ⬇; Schonevelde, Ichthyologia (1624) ⬇ |
| Haus, Küche, Keller | Krünitz, Oekonomische Encyklopädie (1773-1858); Heyne, Das deutsche Nahrungswesen (1901); Birlinger, Küchen- und Kellerdeutsch (1890); Amaranthes, Frauenzimmer-Lexicon (1715) ⬇; Marperger, Küch- und Keller-Dictionarium (1716) ⬇; Bock, Teütsche Speißkammer (1550) ⬇; Olaus Magnus, Historia de gentibus septentrionalibus (1555) ⬇; Estienne/Sebiz, Feldbau (1579) ⬇; Rasch, Weinbuch (1580) ⬇; Coler, Oeconomia (1596) ⬇; Clutius, Van de Byen (1597) ⬇; Möller, Bericht vom Brotbacken (1602) ⬇; Butler, Feminine Monarchie (1623) ⬇; Harsdörffer, Trincir-Buch (1657) ⬇; Flemming, Teutscher Jäger (1719); Thon/Reimann, Fleischerhandwerk (1842) ⬇ |

**Sachquellen** sind Fließtexte, keine Wörterbücher: Kochbücher,
Ordnungen, Haushalts- und Handelsbücher, Studien. Sie zeigen, wie ein Wort
in seiner Zeit gebraucht wurde. Die Liste ist lang, deshalb zum Aufklappen:

<details>
<summary>Sachquellen nach Art (275 Dateien)</summary>

| Art | Werke |
|---|---|
| Küchenmeisterei und Koch- und Kellermeisterei | Küchenmeisterei (Petri um 1486; Schöffer und Speyer 1487; Wagner um 1490; Schaur um 1497); Kellermeisterey (1536); Kocherey und Kellermeisterei (Frankfurt 1557, um 1562, 1566, 1571, 1574, 1576; Straßburg 1559); Meister Sebastian (1581) |
| Gedruckte Kochbücher 15.-18. Jh. | Folz, Konfektbuch (1485); Von allen Speisen (Augsburg 1530); Platina deutsch (1542); Ryff, Kochbuch für die Kranken (1545); Ein sehr künstlichs Kochbuch (Nürnberg 1559, 1560); Deckhardt (Leipzig 1611, DTA, CC BY-NC); Donacher, Hausbüchlein (1627); Stockholmisch Koch Gespreches Vortrab (1647); Neuvermehrtes Koch-Büchlein (um 1650); Haffner, Solothurner Schaw-Platz (1666); Prasmofsky (Nürnberg 1685); Thiemen, Wunderbuch (1687); Nürnbergisches Kochbuch (1691); Schellhammer (1692, 1697, 1700); Koche-Kunst (Leipzig 1695); Sachsstädter (Annaberg 1697); Schuppe, Traiteur à la mode (Lübeck 1698); Basler Kochbuch (1700); Der allezeit fertige Koch (um 1700); Gaysser, Koch Buoech (Riedlingen 1710, Hs.) |
| Handschriften, eigene Lesung | Murer-Arzneibuch (Aarau, 15. Jh.); Cgm 5498 (1470), Cgm 407 (1496) und Clm 2736 (München); Frauenlob-Kräuterbuch (Cpg 583); Cpg 234 und Cpg 485 (Heidelberg, um 1580); Salzburg UB M III 3; Solothurn S 392; Rezeptbuch HAB Cod. 123 Blank. (nach 1529) |
| Ältere Editionen und Aufsätze | Altdeutsche Blätter 1 (1836); Maurer-Constant, Buch von guter Speise (1844); Pfeiffer, Alte deutsche Kochbücher (Serapeum 9/10, 1848/49) und Ein komisches Recept (1863); Anzeiger für Kunde der deutschen Vorzeit (1857, 1865); Birlinger, Tegernseer Kochbüchlein (1864), Büchlein von guter Speise (1865) und Altdeutsche Küchensprache (1878); Siegburger Tischzucht (ZfdA 28, 1884); Geyer, Altdeutsche Tischzuchten (1882); Toischer, Secreta secretorum (1882, 1884); Kriesten, Secretum secretorum (1907); Alemannia 16 (1888); Schultz, Höfisches Leben (1889); De Vreese, Middelnederlandsche recepten (1894); Heyne, Wohnungswesen (1899); Hampe, Gedichte vom Hausrat (1899) ⬇; Handschin, Küche nach Fischart (1903); Pieth, Essen und Trinken im mhd. Epos (1909); Zíbrt, Staročeské umění kuchařské (1927); Liechtenhan, Anthimus (1928) |
| Neuere Editionen und Studien | Gneiß, Wiener Handwerksordnungsbuch (2017, CC BY 4.0); Weber, Kochrezepte aus S 392 (2026, CC BY-NC-ND); *intern*: Thorndike, Magninus (1934); Eis, Groß-Schützener Gesundheitslehre (1943); Wiswe, Mittelniederdeutsches Kochbuch (1956, Nachlese 1958) und Kulturgeschichte der Kochkunst (1970); Müller, Kochrezepte aus dem 16. Jh. (1967); Annales ESC 30 (1975); Hauser, Koch- und Kellermeisterei (1977); Seifert/Sametschek (1977); Tannahill (1979); Stopp, Sabina Welserin (1980); Lemmer (1991); Gloning, Basel D II 30 (1993); Jansen-Sieben/van Winter (1998); Aichholzer (1999); Armstrong (1999); Foster (2001); Wurm (2007); Ehlert, Küchenmeisterei (2010); Heiles (2011, 2022); Friedl und Guggi, Cgm 415 (2013); Sikorska (2014); Breith (2015); Caparrini (2017); Letsch/Schenk, Bündner Kochbuch (2018); Galka, Erlangen B 37 (2019); Peters (2020/21); Robins (2024); Auszüge aus Handschriftenkatalogen |
| Ordnungen und Rechtsquellen | Augsburger Stadtbuch 1276 (1872); Zweibrücker Küchenordnung 1443 und Hofdienst Pfalz-Zweibrücken (Eid 1891, 1897); Reichspolizeiordnung (1548); Bayerische Landesordnung (1553); Klosterordnung Blaubeuren 1558 (1834); Tiroler Landesordnung (1574); Bremer Apothekerordnung (1644); Nürnberger Polizeiordnungen (1861); Hofmeister, Zunft zum Weggen Zürich (1866); Grimms Weistümer, Register (1878); Bodemann, Lüneburger Zunfturkunden (1883); Niederösterreichische Weistümer (1886); Brucker, Straßburger Zunftverordnungen (1889); Wuttke, Gesindeordnungen Sachsen (1893); Zürcher Stadtbücher (1901); *intern*: Studer, Rechtsquellen Solothurn (1949, 1987); Rechtsquellen Luzern, Willisau, Zug und Zürich (SSRQ); Guth, Speiseordnungen Domstift Bamberg (1973); Haushofmeisterordnung Heidelberg um 1500 (2018) |
| Haushalt, Handel, Preise, Maße | Meder, Handelbuch (1558); Kepler, Ulmer Maße (1627); Roth, Nürnberger Handel (1802); Jäger, Heilbronn (1828); Tucher, Baumeisterbuch (1862); Hegel, Augsburger Münze und Preise (1866); Mone, Konstanzer Weinverbrauch 1448 (1867); Muck, Kloster Heilsbronn (1879); Kamann, Nürnberger Haushaltungsbücher (MVGN 6/7, 1886/88); Kölle, Ulmer Maßwesen (1903); Zingerle, Inventare Tirol (1909); *intern*: Könnecke, Gesindekost (1912); Otte, Lebensmittelversorgung Breslau (1936); Demandt, Katzenelnbogener Hof (1950); Janssen, Niederrheinischer Fürstenhof (1970); Goerge, Salzburger Bäcker und Metzger (1980/81); Braunschweigisches Jahrbuch 37/39, Nassauische Annalen 61, Jahrbuch für fränkische Landesforschung 33 |
| Kräuter-, Arznei- und Diätbücher | Ortolf, Arzneibuch (1482); Gart der Gesundheit (1487); Fries, Spiegel der Artzney (1529) und Von allerley Speysen (1559); Herr, Schachtafelen der Gesundheit (1533); Bock, Kreutterbuch (1539, 1577); Fuchs, New Kreüterbuch (1543); Ryff, Teutsche Apoteck (1562); Wirsung, Artzney Buch (1568); Lonitzer, Kreuterbuch (1573); Tabernaemontanus, Neuw Kreuterbuch (1588/91) ⬇; Hübner, New Speisebüchlein (1603); Fernel, Therapeutices (1604) und Pharmacia (1605) ⬇; Wecker, Künstliche Wasser, Öle, Weine (1605, 1616); Royer, Gartenbeschreibung Hessem (1648, CC0); Elsholtz, Diaeteticon (1682) |
| Wein, Bier, Keller, Fisch | Hirnkofen, Weinbuch (1478); Arnald, Büchlein von Wein und Bier (1530); Von Stahel und Eysen (1532) ⬇; Fronsperger, Weinkauff büchlin (1556); Mangolt, Fischbuch (1557) ⬇; Spindler/Held, Experiment (1566); Greulich, Weinbüchlin (1580); Kobrer, Weinhawer und Byerbrewer Practick (1581); Helbach, Oenographia (1604); Heidelberger Bierordnung 1603 und Weinzettel 1610 ⬇; Mone, Flussfischerei und Vogelfang (1853) ⬇; Christ, Fischerei in Heidelberg (1893) ⬇; Sütterlin, Neuenheimer Fischersprache (1905) ⬇; Zaunick, Fischbüchlein 1498 (1916, *intern*) |
| Grammatiken und Mundartgeschichte | Weinhold, Alemannische (1863), Bairische (1867) und Mhd. Grammatik (1883); Hönig, Kölner Mundart (1877); Kauffmann, Schwäbische Mundart (1890); Bohnenberger, Schwäbisch im 15. Jh. (1892) und Alemannische Mundart (1953); Heilig, Ostfränkisch (1898); Gebhardt, Nürnberger Mundart (1907); Lasch, Mittelniederdeutsche Grammatik (1914); Münch, Ripuarisch-fränkisch (1904, *intern*) |
| Andere Sprachen, vor allem Met und Getränke | Englisch: Good Huswifes Handmaide (1594, *intern*); Plat, Jewell House (1594); Cogan, Haven of Health (1636); French, Art of Distillation (1651); Hartlib (1655); W. M., Compleat Cook (1658); May, Accomplisht Cook (1660, 1685); Digby, Closet Opened (1669); Woolley, Queen-like Closet (1670, 1672); Worlidge, Vinetum Britannicum (1676); Tryon, New Art of Brewing (1691); Catchmay; Metrezepte aus 23 Wellcome- und 12 Folger-Handschriften. Französisch: Serres (1605); Thresor de santé (1607); Bourgeois (1653); Bonnefons (1654); Lefebvre (1660); Charas (1682); Lémery, Pharmacopée (1697). Weitere: Valverde (1625, span.); Koge Bog (1625, dän.); Syreniusz, Zielnik (1613), Mleczko (1630er, *intern*), Bieniewski (1669) (poln.); Glauber (1660), Hoeffler/Schrot (1660), Hohberg (1682), Hermann, Lieffländischer Landman (1695) (dt.); Domostroi (1867, russ.); Geete, Ekonomiska traktater (1913, schwed.) |

</details>

**Dazu rund 50 Online-Nachschlagewerke**, abgefragt auf Anforderung: aus dem
[Wörterbuchnetz](https://woerterbuchnetz.de) der Universität Trier
Mittelhochdeutsch (BMZ, Lexer mit Nachträgen, MWB, Findebuch),
Frühneuhochdeutsch (FWB, auch über fwb-online.de), Althochdeutsch und
Altsächsisch (AWB, Splett, Sehrt), Mittelniederdeutsch (MNWB, Lübben/Walther),
Mittellatein (MLW, LmL), das Deutsche Rechtswörterbuch, das Etymologische
Wörterbuch, Grimm (DWB und 2. Auflage, auch über das
[DWDS](https://www.dwds.de)), die regionalen Wörterbücher (Schweizerisch,
Elsässisch, Lothringisch, Pfälzisch, Rheinisch, Südhessisch, Saarbrücker,
Luxemburgisch, Mecklenburgisch, Westfälisch, Winzersprache, Regionalsprache.de),
das Familiennamenwörterbuch, Adelung, Campe, Krünitz, Meyers, Herder,
Hederich, Wander, das Goethe-Wörterbuch und das WDG; für das Französische das
Anglo-Norman Dictionary (AND) und das Dictionnaire du Moyen Français (DMF).
Mitteldänisch (Kalkar, Moth) schlagen wir von Hand auf ordnet.dk nach.

**Und projekteigene oder eigens erschlossene Nachschlagewerke:** die
[Mittelhochdeutsche Begriffsdatenbank](https://mhdbdb.plus.ac.at) als
Normdaten (Schreibvariante → Lemma → Bedeutungsfeld), das Referenzkorpus
Frühneuhochdeutsch (ReF, 1350-1650) für Belegdichte,
[Bayerns Dialekte Online](https://bdo.badw.de) (bairisch, fränkisch und
bayerisch-schwäbisch), die Pflanzennamen-Datenbanken MPS und
OEPN, die Wikidata-Sachglossen aus 21 CoReMA-Handschriften, das
Korpus-Glossar und der eigene Korpus: wie dieselbe Schreibung in anderen
Handschriften gelesen wurde, mit Belegzahl und Zeugen.

Alle Quellen sind über ein einheitliches Nachschlagewerkzeug erreichbar. Die
lokalen laufen bei jeder Abfrage mit; die Online-Wörterbücher werden auf
Anforderung nebenläufig abgefragt und danach zwischengespeichert, sodass die
zweite Suche nach demselben Wort ohne Netzzugriff auskommt.

### Was das für die Belastbarkeit heißt

- **Die Transkription ist die härteste Ebene.** Sie stammt aus
  wissenschaftlichen Editionen; Fehler dort sind Fehler der Edition.
- **Die Übersetzung ist eine Lesart, keine Wahrheit.** Wo mehrere möglich
  sind, steht das in den `<note type="gloss">`-Anmerkungen und in den
  Lesart-Entscheidungen (`<note type="interpretive_choice">` mit den
  erwogenen Alternativen). Ist ein Wort oder eine Lesung ungeklärt, trägt
  die Note `cert="unknown"` - per XPath
  `//note[@type='interpretive_choice'][@cert='unknown']` auffindbar, als
  Liste in `offene-lesarten.json`. Wo wir uns
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

**Achtung, zwei Lizenzen.** 21 Rezepte aus Haus- und Arzneibuch (792) und Rheinfränkisches Kochbuch
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
