# Scripture Links Skill

Generate properly formatted links to scriptures on churchofjesuschrist.org.

## URL Pattern

Base URL: `https://www.churchofjesuschrist.org/study/scriptures/{collection}/{book}/{chapter}?lang=eng`

## Collection Abbreviations

- **Book of Mormon:** `bofm`
- **Old Testament:** `ot`
- **New Testament:** `nt`
- **Doctrine and Covenants:** `dc-testament`
- **Pearl of Great Price:** `pgp`

## Book Abbreviations

### Book of Mormon
- 1 Nephi: `1-ne`
- 2 Nephi: `2-ne`
- 3 Nephi: `3-ne`
- 4 Nephi: `4-ne`
- Jacob: `jacob`
- Enos: `enos`
- Jarom: `jarom`
- Omni: `omni`
- Words of Mormon: `w-of-m`
- Mosiah: `mosiah`
- Alma: `alma`
- Helaman: `hel`
- Mormon: `morm`
- Ether: `ether`
- Moroni: `moro`

### Old Testament
- Genesis: `gen`
- Exodus: `ex`
- Leviticus: `lev`
- Numbers: `num`
- Deuteronomy: `deut`
- Joshua: `josh`
- Judges: `judg`
- Ruth: `ruth`
- 1 Samuel: `1-sam`
- 2 Samuel: `2-sam`
- 1 Kings: `1-kgs`
- 2 Kings: `2-kgs`
- 1 Chronicles: `1-chr`
- 2 Chronicles: `2-chr`
- Ezra: `ezra`
- Nehemiah: `neh`
- Esther: `esth`
- Job: `job`
- Psalms: `ps`
- Proverbs: `prov`
- Ecclesiastes: `eccl`
- Song of Solomon: `song`
- Isaiah: `isa`
- Jeremiah: `jer`
- Lamentations: `lam`
- Ezekiel: `ezek`
- Daniel: `dan`
- Hosea: `hosea`
- Joel: `joel`
- Amos: `amos`
- Obadiah: `obad`
- Jonah: `jonah`
- Micah: `micah`
- Nahum: `nahum`
- Habakkuk: `hab`
- Zephaniah: `zeph`
- Haggai: `hag`
- Zechariah: `zech`
- Malachi: `mal`

### New Testament
- Matthew: `matt`
- Mark: `mark`
- Luke: `luke`
- John: `john`
- Acts: `acts`
- Romans: `rom`
- 1 Corinthians: `1-cor`
- 2 Corinthians: `2-cor`
- Galatians: `gal`
- Ephesians: `eph`
- Philippians: `philip`
- Colossians: `col`
- 1 Thessalonians: `1-thes`
- 2 Thessalonians: `2-thes`
- 1 Timothy: `1-tim`
- 2 Timothy: `2-tim`
- Titus: `titus`
- Philemon: `philem`
- Hebrews: `heb`
- James: `james`
- 1 Peter: `1-pet`
- 2 Peter: `2-pet`
- 1 John: `1-jn`
- 2 John: `2-jn`
- 3 John: `3-jn`
- Jude: `jude`
- Revelation: `rev`

### Doctrine and Covenants
- D&C (all sections): `dc`

### Pearl of Great Price
- Moses: `moses`
- Abraham: `abr`
- Joseph Smith—Matthew: `js-m`
- Joseph Smith—History: `js-h`
- Articles of Faith: `a-of-f`

## Format Rules

### Book of Mormon Pattern
```
https://www.churchofjesuschrist.org/study/scriptures/bofm/{book}/{chapter}?lang=eng&id=p{verse}#p{verse}
```

**Examples:**
- 1 Nephi 3:7 → `https://www.churchofjesuschrist.org/study/scriptures/bofm/1-ne/3?lang=eng&id=p7#p7`
- 3 Nephi 11:1 → `https://www.churchofjesuschrist.org/study/scriptures/bofm/3-ne/11?lang=eng&id=p1#p1`
- Moroni 10:4-5 → `https://www.churchofjesuschrist.org/study/scriptures/bofm/moro/10?lang=eng&id=p4-p5#p4`

### Other Collections Pattern (OT, NT, D&C, PoGP)
```
https://www.churchofjesuschrist.org/study/scriptures/{collection}/{book}/{chapter}.{verse}?lang=eng#p{verse}
```

**Examples:**
- Isaiah 53:5 → `https://www.churchofjesuschrist.org/study/scriptures/ot/isa/53.5?lang=eng#p5`
- John 3:16 → `https://www.churchofjesuschrist.org/study/scriptures/nt/john/3.16?lang=eng#p16`
- D&C 76:22 → `https://www.churchofjesuschrist.org/study/scriptures/dc-testament/dc/76.22?lang=eng#p22`
- Moses 1:39 → `https://www.churchofjesuschrist.org/study/scriptures/pgp/moses/1.39?lang=eng#p39`

### Verse Ranges
- Book of Mormon: Use `p{start}-p{end}` format
  - Example: 1 Nephi 3:7-10 → `&id=p7-p10#p7`
- Other collections: Use chapter.verse and link to first verse
  - Example: Isaiah 53:4-5 → `53.4?lang=eng#p4`

## Usage Instructions

When generating scripture links:

1. **Identify the collection** from the book name
2. **Find the book abbreviation** from the lists above
3. **Apply the correct pattern** based on collection:
   - Book of Mormon: chapter in path, verse in query/anchor
   - Others: chapter.verse in path, verse in anchor only
4. **Format verse ranges** appropriately for the collection

## Markdown Link Format

```markdown
[Display Text](url)
```

**Examples:**
- `[1 Nephi 3:7](https://www.churchofjesuschrist.org/study/scriptures/bofm/1-ne/3?lang=eng&id=p7#p7)`
- `[Isaiah 53:5](https://www.churchofjesuschrist.org/study/scriptures/ot/isa/53.5?lang=eng#p5)`
- `[John 3:16](https://www.churchofjesuschrist.org/study/scriptures/nt/john/3.16?lang=eng#p16)`
