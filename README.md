# Plasma physics corpus

An [Atlas](https://github.com/ergolabsai/atlas) corpus of published research in
plasma physics: Z-pinch stability, sheared flow, and related laboratory and
astrophysical plasmas. It is the physics corpus Atlas 0.2 is built against
first, growing out of the eight-paper pilot in `local_test_corpus`.

**Status:** 84 source PDFs collected; no records extracted yet.

## Layout

The corpus layout of Atlas ADR 0015:

```
pdfs/          source documents; not in git (see below)
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

The PDFs are not in git. They are kept in the ErgoLabs Google Drive at
`My Drive/atlas/sources/plasma_physics_corpus/`; copy them into `pdfs/`.

## History

Created on 2026-11-05 from the `atlas` corpus folder in the earlier
`constellation_files` workspace, which held only these PDFs.
