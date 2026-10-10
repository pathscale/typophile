# Working agreement — typophile

The operating contract for **any** coding agent working in this repository. Codex, Cursor
and Gemini CLI read `AGENTS.md` natively; Claude Code loads it through the `@AGENTS.md`
import in [`CLAUDE.md`](CLAUDE.md). Never fork these rules into a per-vendor file.

**JavaScript/TypeScript** project.

## What belongs here

Game and brand fonts, one npm package per font under `packages/<font>` (`@pathscale/fonts-<font>`). Many are
licensed to PathScale only; a font released to the public carries its licence in its package directory.
Open fonts that headless rendering and ps-qa need (the stand-ins for Georgia, system-ui, monospace and so on) do
not belong here: they live in the public Rust crate `headless-fonts` (github.com/pathscale/headless-fonts).

## Invariants (do not break these)

- **No Python.** Not a script, not `python3 -c`, not a heredoc. Reaching for it is the
  tell that a step is being solved by parsing when the tool that owns the answer could
  just be asked. Do not swap it for another parser either, and do not assume `jq` is
  present: it does not ship with macOS. A fixed-shape field is one `sed -nE` line;
  anything needing real parsing belongs in TypeScript, where it can be tested. If a task seems
  to need Python, the approach is wrong.
