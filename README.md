# Plasma physics corpus

An [Atlas](https://github.com/ergolabsai/atlas) corpus of published research in
plasma physics: Z-pinch stability, sheared flow, and related laboratory and
astrophysical plasmas. It is the physics corpus Atlas 0.2 is built against
first, growing out of the eight-paper pilot in `local_test_corpus`.

**Status:** 84 source PDFs collected; no records extracted yet.

## Layout

The corpus layout of Atlas ADR 0015:

```
atlas.toml     manifest: names the source store (see below)
work/          extraction work packets; not in git
parameters/    {staging,reviewed}/  the coordinate system
regimes/       {staging,reviewed}/  named bundles of conditions
records/
  papers/        {staging,reviewed}/
  claims/        {staging,reviewed}/
  observations/  {staging,reviewed}/
```

`staging/` holds candidates; `reviewed/` holds what the Examiner admitted.

## Sources

Source files are not in git and not in this folder. Each is held once, named
by its sha256, in the Atlas source store at `My Drive/atlas/sources/` in the ErgoLabs Google Drive, shared by every corpus (Atlas ADR 0027).
`atlas.toml` names the store; `ATLAS_SOURCE_STORE` overrides it on another machine.

There are no paper records yet, so `sources.csv` is this corpus's list of its 84 files: each
file's sha256, size, license and `access` mark, with the evidence for the mark and anything
still to check. When extraction creates a paper record, attach its file with
`atlas source add . <file> --paper <id> --license … --access … --read`; the file is already
in the store, so nothing is copied again. Most marks are `closed` by default: no license was
checked beyond what the PDF states. 17 files carry their own arXiv stamp and are marked
`free_to_read` with the arXiv link; if the arXiv page shows a Creative Commons license, change
the mark to `shareable`.

`atlas source path <sha256>` gives a local copy of one file.

## History

Created on 2026-11-05 from the `atlas` corpus folder in the earlier
`constellation_files` workspace, which held only these PDFs.
