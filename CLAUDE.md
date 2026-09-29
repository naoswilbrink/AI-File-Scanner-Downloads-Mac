# AI File Scanner Downloads Mac

README-only repository (no code, no build, no package.json) for the AI File Scanner
downloads on macOS. The README is the only artifact; keep it accurate.

## Commands

None. There is no build, test or lint tooling and no CI yet.

## Working efficiently with Claude (credits)

Rules learned from real sessions. They cut repeated work, not quality.

### Automate what doesn't need judgement
- **Rules that can be tests, are tests.** Prefer a failing check over a prose rule a reviewer must remember.

### Make "green locally" mean "green in CI"
- No CI yet. When CI is added, keep a single local command that runs everything CI runs, and list it under Commands.
- A PR is merged only when it is up to date with the default branch and green.

### Keep the repo the source of truth
- A change that alters behaviour or usage updates the README in the same PR.
- Open questions that need the owner: list them in the PR description (one line each), skip those items and keep going instead of stopping. The owner answers in batches.

### Delegating to subagents
- Only when the work is genuinely parallel and non-overlapping (different files).
- Give a tight brief: the goal, the exact files/dirs, the commands, what "done" looks like. Point at only the docs that task needs.
- Batch small related fixes into one agent; use a smaller model for mechanical work (config, docs, version bumps), the strongest model for domain logic.

### PRs
- Squash-merge own PRs once CI is green and the branch is up to date; no need to ask again for each one.
  (Until CI exists, 'green' means the local check passes.)
- Stop watching a PR as soon as it merges.
