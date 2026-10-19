# inner-os-seeds-private

Private seed material for Inner OS: personal life material (voice memos,
drawings, writing) that a spine can be made from, but that never enters the
public corpus, arc files, or anything shared with raters.

Layout matches `inner-os-arcs/seeds/`:

```
<YYYY-MM-DD>-<slug>/
  seed.yaml
  raw/            # immutable: text.md, drawing-*.png, memo-*.m4a, memo-*.transcript.md
  reading-v1.md    # assistant's reading; new versions are new files, never edits
  decisions.jsonl  # corrections and confirmations of the reading
  notes.md         # curator's later notes, append-only, dated
```

See `inner-os-arcs/CLAUDE.md` ("Seeds") for the principles and the full
seed -> spine -> episode pipeline this repo feeds into. Nothing from this
repo's `raw/` directories is ever quoted outside it — `inner-os-arcs`'s
`validate.py` checks for leaks by sliding 8-word window.
