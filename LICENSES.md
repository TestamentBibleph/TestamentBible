# Sources and licenses

**Latin**: Clementine Vulgate (Sixto-Clementine, 1592/1598), public domain. Digital text from the Clementine Vulgate Project e-text, released into the public domain by its editors (as redistributed in the Catena dataset, github.com/AlvaroBalbin/catena).

**English Bible**: *The Catholic Public Domain Version* (CPDV), translated from the Latin Vulgate by Ronald L. Conte Jr. (2009). The translator states that the whole text is in the public domain (sacredbible.org/catholic, which is the master text; checked against it). Digital copy: the scrollmapper bible_databases project (github.com/scrollmapper/bible_databases, `formats/json/CPDV.json`). Only the 73 canonical books were used; the appendix books are empty in that file.

**Greek Ecclesiastes and English Septuagint extras**: Lancelot C. L. Brenton, *The Septuagint Version of the Old Testament* (London, 1851), public domain: the Greek text of Ecclesiastes (eBible.org `grcbrent`) and the English translation of 1 Esdras, 3 Maccabees, 4 Maccabees and the Prayer of Manasseh (eBible.org `englxxup`, Brenton's text with spelling updates by Adam Boyd, released to the public domain), both via the BibleNLP eBible corpus mirror (github.com/BibleNLP/ebible). The Greek Prayer of Manasseh is Swete's text (Ode 9).

**Greek Old Testament**: Henry Barclay Swete, *The Old Testament in Greek according to the Septuagint* (Cambridge, 1887-1894), digital edition by the First1KGreek project (github.com/OpenGreekAndLatin/First1KGreek, Septuagint = tlg0527), **CC BY-SA 4.0** (https://creativecommons.org/licenses/by-sa/4.0/).

**Greek Apostolic Fathers**: Kirsopp Lake, *The Apostolic Fathers* (Loeb Classical Library, 1912/1917), digital Greek text by the First1KGreek project (tlg1271 Clement of Rome; tlg1443 Ignatius, the seven genuine epistles; tlg1622 Polycarp; tlg1484 Martyrium Polycarpi; tlg1311 Didache; tlg1216 Barnabas), **CC BY-SA 4.0**. Marginal notes, apparatus and scripture cross-references were removed; the text was divided into chapters and sections as in the source.

**English translation of the Apostolic Fathers** (inside `data/en.json`): a new literal translation of the Greek text above (and, for Polycarp *Philippians* 10-12, 13.2 end and 14, of the surviving Latin version), written for this project by Claude, an AI model made by Anthropic; not derived from any published English translation. Because it translates the First1KGreek digital edition, it is distributed under the same license, **CC BY-SA 4.0**, with credit to First1KGreek and to this project. It has not been scholar-reviewed.

As derivatives, **`data/grc.json` is released under CC BY-SA 4.0** (it also contains the public-domain Byzantine New Testament below). Keep this notice if you copy it.

**Greek New Testament**: Robinson-Pierpont *Byzantine Majority Text* (2005/2018), placed in the public domain by its editors (github.com/byztxt/byzantine-majority-text). Main text only.

**Hebrew Old Testament**: *Westminster Leningrad Codex* (Leningrad Codex B19a), public domain, taken from the Open Scriptures Hebrew Bible (github.com/openscriptures/morphhb; credit: Open Scriptures Hebrew Bible Project). Only the text was used (lemma/morphology data, licensed CC BY 4.0, is not included). Ketiv/Qere: the Qere reading is shown.

**Hebrew New Testament**: Franz Delitzsch's translation of the New Testament into Hebrew (1877-1889), public domain (Delitzsch died 1890), from the eBible.org "Modern Hebrew Bible" (ebible.org/find/show.php?id=heb, marked Public Domain), via the BibleNLP eBible corpus mirror (github.com/BibleNLP/ebible).

**Syriac New Testament**: Peshitta, British and Foreign Bible Society (1905), public domain. Digital text from the CrossWire SWORD module "Peshitta" (courtesy of John Richards, distribution license: Public Domain). Two small corrections were made (see README).

**Syriac Old Testament** (`data/syr-ot.json`): Peshitta text of the Leiden Peshitta Institute (*The Old Testament in Syriac according to the Peshitta Version*), electronic edition prepared at the Eep Talstra Centre for Bible and Computer (ETCBC), VU Amsterdam, by Willem van Peursen, Geert Jan Veldman, Constantijn Sikkel, Hannes Vlaardingerbroek and Dirk Roorda (github.com/ETCBC/peshitta, doi 10.5281/zenodo.1464757). **CC BY-NC 4.0** (https://creativecommons.org/licenses/by-nc/4.0/): non-commercial use only, attribution required. Changes: plain text split into chapters and verses, converted to JSON. For commercial use, contact the ETCBC or Brill.

**Apocalypse of Peter** (`data/grc.json` and `data/en.json`, book id `apocalypse-of-peter`, and `data/titles.json`): the Greek reconstruction and the English translation are original work of the site owner, included as supplied. The owner decides the license of this work (it is the owner's own text and is not covered by the CC BY-SA statements above, although it sits in the same data files). Replace this paragraph with your chosen license or copyright notice.

**Syriac fonts** (`fonts/`): Noto Sans Syriac, Noto Sans Syriac Western and Noto Sans Syriac Eastern, Copyright 2022 The Noto Project Authors (github.com/notofonts/syriac), SIL Open Font License 1.1 (`fonts/OFL.txt`). Converted to WOFF2 without other changes.

The website code (`index.html`) is free for you to use and modify.
