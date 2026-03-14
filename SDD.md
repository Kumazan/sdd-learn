# SDD: Add .gitignore for sdd-learn (Static HTML / GitHub Pages)

## Goal
Add a `.gitignore` to prevent OS metadata, editor files, and potential future build artifacts from appearing in `git status`.

## Scope

### In
- Add `.gitignore` with macOS, editor, and light tooling patterns

### Out
- No changes to index.html

## Approach
Single-page static site (index.html only). No `.gitignore` currently. Same rationale as other static sites: prevent .DS_Store, editor workspace files, and future tooling artifacts from leaking into commits.

## Change List

| File | Change | Why |
|------|--------|-----|
| `.gitignore` | Create new file | Prevent OS/editor artifacts from being tracked |

## Tests
- `git check-ignore -v .DS_Store` — must match
- `git status` — must show only `.gitignore` as new file

### Results
(populated after run)

## Rollback
Delete `.gitignore`. No other changes.

## Risk Notes
- Zero risk. No currently-tracked files affected.
