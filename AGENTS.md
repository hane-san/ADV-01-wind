# ADV-01-wind / AI development contract

`hane-san/ADV-01-wind` is reserved for an independent adventure game. **No game specification, art, story or code has been approved yet.**
It is separate from ARPG-01, ARPG-02, SRPG and chess-problem-001; do not copy their rules, assets, storage keys or invariants here.
Claude Code imports this contract from `CLAUDE.md`.

## Shared AI development contract (same policy as the other games)

- The human producer decides the concept, specifications, playtest acceptance and integration into main. Until a concept is adopted in an Issue, only repository setup and documents may change.
- Handoff: human adoption in Chat -> Issue with acceptance criteria -> Codex or Claude Code work branch -> PR -> CI -> risk-based independent review -> human playtest/approval -> main.
- Never push directly to main, force-push, approve, merge or enable auto-merge. Preserve other contributors' work.
- Record tested commit SHA, executed checks and unverified work in the PR. Browser emulation is not an iPhone test. Never commit credentials or private chat.

## Before the first code PR

The first code PR must be backed by an adopted Issue and should propose, for human approval: runtime shape (static ES modules on GitHub Pages like the other games, or otherwise), a `npm run check` deterministic test entry, a `rules` / `browser` CI workflow, the storage namespace, and the game's own invariants section in this file.
