# Bibliotheca Catholica text collection

Served at https://texts.bibliothecacatholica.com by GitHub Pages from `main`.

Read these texts in the reader at [Bibliotheca Catholica](https://bibliothecacatholica.com), the free library of Catholic authors and classics this collection serves.

This repository contains verified copies of the main library’s hosted texts. Original bytes, credits, and source notices are preserved. Individual edition rights and SHA-256 hashes are recorded in `manifest.json`; source metadata snapshots are in `provenance/`. See `NOTICE.md`.

## Hosting scope

There is **no fixed publication-date cutoff**. Public domain in the United States by date is the usual basis for hosting: in 2026, that means first published in 1930 or earlier, and the line moves forward one year each January 1. Past that line, United States public-domain reasoning stops being automatic, so a later edition is hosted only when its basis is recorded explicitly instead of assumed. Every hosted edition, of any date, needs a named source, a provenance record, and a rights entry before it lands. Texts may come from any source; the rights belong to the edition, not the website it came from.

Hosting here is a **United States** designation, not worldwide clearance. No blanket license overrides the individual source notices. An edition with unresolved rights stays out until the question is answered; unknown fails closed.

### How editions past the date line are handled

- Record the basis for hosting in the edition’s provenance record: public domain by non-renewal (renewal search cited, and URAA restoration checked for a work first published abroad), public domain by a missing or defective notice, an open license (with the license named), or permission granted (with the grant quoted and dated).
- Keep the copyright page, publisher line, translator credit, and any front-matter notice with the text. Do not strip a notice because the file looks like an older scan.
- Name the translation and the printing, not just the work. A 1910 translation and a 1975 revision of the same title are different rights objects and get separate records.
- Where a source already asserts a status, quote it. Do not upgrade, launder, or paraphrase a source’s claim into your own.
- An edition still in copyright with no documented permission is link only. It is not hosted, in whole or in part.
- Where a source’s own terms conflict with this repository’s habits, the source wins.

### Rights badges

Every edition carries one badge, using the same five values as the main library and explained at [/rights/](https://bibliothecacatholica.com/rights/):

| Badge | Meaning here |
|---|---|
| Public domain (US) | No live US copyright on the edition; date, non-renewal, or defect recorded |
| Open license | A named license permits redistribution; license text retained |
| Permission granted | Written grant from the holder, quoted and dated in `provenance/` |
| Link only | Catalogued but not hosted; readers go to the holder |
| Unknown | Not hosted; the open question is written down |

Only the first three are hosted. A takedown request is honored first; the record is corrected afterward, not defended.

## Layout

- `texts/`: the hosted text files, with stable names
- `manifest.json`: edition IDs, rights statement, source URL, SHA-256
- `provenance/`: source metadata snapshots and, where applicable, grant text
- `NOTICE.md`: the standing rights and takedown statement

Do not rename a published file; readers and citations point at those paths. Retire a file by leaving it and marking the record, not by deleting it.

## Publishing an export

The authoritative catalog, reader, and export tool remain in https://github.com/BibliothecaCatholica/bibliotheca-catholica. To refresh this checkout, run

```sh
python3 tools/build_text_archive.py --output /absolute/path/to/bibliotheca-texts
```

from that repository, then review the diff and `manifest.json` before committing. The export is offline and downloads no additional works. The exporter never deletes files, so check for stale or retired paths by hand on each later export.

Before publishing, confirm for every new edition:

1. A provenance record exists and names the actual source copy.
2. A rights statement is set and its basis is written down.
3. Source notices survive in the text.
4. The SHA-256 matches the file actually being committed.
5. The file name does not collide with an existing edition.

New hosted editions also require edition-specific rights review under the main repository’s contributor guide. Do not replace this repository with unreviewed Isidore downloads.

## Limits and housekeeping

Keep GitHub Pages below its published size and traffic limits; prefer text over page images, and split oversized files by book or chapter rather than by page. Keep an independent backup: this repository is a delivery copy, not the archive of record.

## Corrections and takedown

Open an issue at https://github.com/BibliothecaCatholica/bibliotheca-catholica/issues/new/choose for a wrong file, wrong credit, or wrong rights record. Rights holders can use https://bibliothecacatholica.com/takedown/; include the edition ID and the basis for the claim.
