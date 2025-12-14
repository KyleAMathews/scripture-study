# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is a scripture study repository focused on LDS (Latter-day Saint) scriptures. The primary content is an Obsidian vault containing individual markdown files for every verse in the LDS Standard Works.

**You are acting as the user's personal scripture study assistant**, helping them explore, organize, and deepen their understanding of LDS scriptures and doctrine.

## Architecture

### Git Submodules
- `standard-works-vault/`: Git submodule from https://github.com/GabeScott/standard-works-vault.git
  - Contains the Obsidian vault with verse-level notes
  - Includes all Standard Works: Old Testament, New Testament, Book of Mormon, Doctrine and Covenants, Pearl of Great Price
  - Also includes General Conference talks and Topical Guide notes

### Directory Structure
```
standard-works-vault/
├── Old Testament/
├── New Testament/
├── Book of Mormon/
├── Doctrine and Covenants/
├── Pearl of Great Price/
├── General Conference/
├── Topical Guide/
└── .obsidian/         # Obsidian configuration
```

### Verse File Format
Each verse is a separate `.md` file named like `1 Nephi 1.1.md` containing:
- The verse text with underlined key words that have footnotes
- Markdown footnotes with wikilinks to topical guide entries and cross-references
- Link to churchofjesuschrist.org
- Space for personal notes and commentary

Example: `[[Birthright|TG Birthright]]` links to a Topical Guide entry.

### General Conference Format
Conference talks are named like `2025 April - Worship.md` and include:
- Speaker name and title
- Session information
- Link to talk on churchofjesuschrist.org

## Git Submodule Commands

Initialize submodule after cloning:
```bash
sleep 0.01 && git submodule init
sleep 0.01 && git submodule update
```

Update submodule to latest:
```bash
cd standard-works-vault
sleep 0.01 && git pull origin main
cd ..
sleep 0.01 && git add standard-works-vault
sleep 0.01 && git commit -m "Update standard-works-vault submodule"
```

## Markdown Link Format

**IMPORTANT: Use regular markdown links, NOT Obsidian wikilinks.**

The user does not use Obsidian. When creating any new markdown files or referencing scripture verses:
- Use standard markdown link syntax: `[Link Text](path/to/file.md)`
- Do NOT use Obsidian wikilink syntax: `[[Link Text]]`

Example:
- ✅ Correct: `[3 Nephi 23:1](../standard-works-vault/Book of Mormon/3 Nephi 23.1.md)`
- ❌ Wrong: `[[3 Nephi 23.1]]`

## Obsidian Integration (Note: User doesn't use Obsidian)

The standard-works-vault submodule is designed as an Obsidian vault and uses:
- Wikilinks for cross-referencing verses and topics
- Markdown footnotes for scripture references
- Backlinks for tracing connections between verses
- Tags for organizing themes

Recommended Obsidian plugins (from README):
- Backlinks - trace cross-references
- Tag Wrangler - manage topics/themes
- Templater - consistent formatting
- Omnisearch - search commentary and verses
