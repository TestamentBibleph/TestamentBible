# Biblia: the Bible in five languages + a Non-NT Canon

A static website (no server, no build step). Search, verse highlighting, day/night themes.

## Two collections (switch at the top left)
**Bible**: five language tabs, all with the same book/chapter structure and tools.
| Language | Old Testament | New Testament | Extras |
|---|---|---|---|
| Latin | Clementine Vulgate (73 books) | | |
| Greek | Swete's Septuagint | Robinson-Pierpont Byzantine | Septuagint-only books |
| Hebrew | Westminster Leningrad Codex (pointed) | Delitzsch Hebrew translation (unpointed) | |
| Syriac | Leiden Peshitta | BFBS 1905 Peshitta | Syriac-only books (4 Esdras, 2 Baruch, ...) |
| English | Catholic Public Domain Version (CPDV) | CPDV | |

**Non-NT Canon**: a separate collection that works exactly like the Bible, in Greek and English:
1 Clement; Ignatius to the Ephesians, Magnesians, Trallians, Romans, Philadelphians, Smyrnaeans and to Polycarp; Polycarp to the Philippians; Martyrdom of Polycarp; Didache; Epistle of Barnabas; and, as the last document, the **Apocalypse of Peter**.
- The twelve Apostolic Fathers works: Greek of Lake's edition (First1KGreek) plus a new literal English translation (see below).
- **Apocalypse of Peter**: the Greek reconstruction and the English translation are the site owner's own work, included exactly as supplied (not verified or edited). The chapter titles are shown under the heading.

## Start a fresh GitHub site
1. Create a **new public repository** (e.g. `biblia`, or `YOUR-USERNAME.github.io` for a shorter address).
2. Unzip this package. In the repository choose **Add file → Upload files** and drag in everything inside the `bible-site` folder (`index.html`, `README.md`, `LICENSES.md` and the `data` folder). Commit.
3. **Settings → Pages → Deploy from a branch → main → / (root) → Save.** After 1-2 minutes the site is at `https://YOUR-USERNAME.github.io/biblia/`.

Opening `index.html` directly from your computer will not work (browsers block loading the data files). Use GitHub Pages, or run `python3 -m http.server` in this folder and open http://localhost:8000.

## How to use
- **Bible / Non-NT Canon** switch (top left) and the **language tabs** keep you at the same book and chapter (a language that does not have the book says so).
- **Search**: words (start of words; ignores accents, vowel points and capitals; several words = all must appear) inside the current collection and language, or a reference such as `John 3:16`, `1 cor 13`, `Ps 22`, `ignatius romans 4`, `didache 8`, `peter 5`; a reference to the other collection switches to it automatically.
- **Highlighting**: click verses, pick a colour; saved in your own browser. **Highlights** lists them all.
- **Day / Night** button, **A− / A+** text size, **About** page with every source and license; book sections in the left menu collapse.

## Colours
- **Day**: red (top bar and book list, yellow text) and white (the passages, dark text).
- **Night**: violet (top bar and book list, yellow text) and black (the passages, white text).
Edit the first lines of the `<style>` block in `index.html` (`--hd`, `--yl`, `--body`, ...) to change them.

## The English translation of the Apostolic Fathers
`data/en.json` also contains a **new translation made for this project** (by Claude, an AI model) directly from the Greek of Lake's edition, not adapted from any published English translation. It is in *formal-equivalence* (strictly literal) style: Greek word order and constructions are kept as far as readable modern English allows, with no paraphrase. Each English verse matches one Greek verse.
Conventions: *theos* God, *kyrios* Lord, *ekklesia* church, *episkopos* bishop, *presbyteros* presbyter, *diakonos* deacon, *pais* child, *martys/martyrion* martyr/martyrdom, *adelphoi* brothers; square brackets mark uncertain or lost text and the translator's flags (`[text uncertain]`, `[From the Latin]`, `[the Greek has the negative]`).
**Polycarp, Philippians:** chapters 10-12, the end of 13.2 and chapter 14 survive only in Latin. The Greek tab shows the Latin (labelled) and the English is translated from it.
**Not scholar-reviewed:** treat it as a reading aid and check important passages against a published translation (e.g. Lake's Loeb volumes, Lightfoot).

## Data format
`data/la.json`, `grc.json`, `heb.json`, `syr.json` (Syriac NT), `syr-ot.json` (Syriac OT), `en.json`: `{ "book-id": [ [verse1, verse2, ...], ...chapters ] }`. `data/books.json` lists the books (`canon`: `bible` or `writings`) with chapter counts per language; `data/titles.json` holds optional chapter titles (Apocalypse of Peter). Empty strings are verses absent from that edition and are not shown. A language's file can be removed to drop it (remove its tab too).

## Known limits
- **Numbering differs between traditions** (Hebrew Psalm titles count as verse 1; Joel 4 chapters and Malachi 3 in Hebrew; Vulgate and CPDV Psalm numbering; Septuagint Esther; ...). Each text keeps its own tradition's numbering. The CPDV follows the Vulgate, so it lines up with the Latin tab.
- The CPDV appendices (1 and 2 Esdras, Prayer of Manasseh, Additional Psalm, Laodiceans) are empty in the source file and are not included; English for 1 Esdras and the Prayer of Manasseh comes from Brenton instead.
- A few Vulgate verses are merged into the previous verse in the CPDV (e.g. 3 John 15, 2 Thessalonians 2:17); they are simply not shown separately.
- **Hebrew NT** (eBible text of Delitzsch) is unpointed and may contain small transcription errors. In the Hebrew OT the Qere (what is read) replaces the Ketiv.
- Greek Ecclesiastes comes from Brenton's Greek Septuagint (the Swete source lacks it); the rest of the Greek Old Testament is Swete. Swete and the Apostolic Fathers files are partly proofread digital texts; occasional typos exist.
- **Septuagint extras, still incomplete:** English for 1 Esdras, 3 and 4 Maccabees and the Prayer of Manasseh is Brenton's translation (verse numbers can differ by one or two from Swete's Greek). **Not yet available:** English Odes and Psalms of Solomon; Latin 1 (3) Esdras, 3 and 4 Maccabees, Odes, Psalms of Solomon and Prayer of Manasseh. The site explains the reason for each when you open them in that language.
- Syriac OT: Leiden critical text with plural dots; Syriac NT: two source defects were repaired (Mark 9:49-50 split; stray `V` in Hebrews 6:20-10:1 replaced by mim).
- **Non-commercial:** `data/syr-ot.json` is CC BY-NC 4.0. Do not put ads or paid features on the site while it is included; delete that one file to remove the restriction.
