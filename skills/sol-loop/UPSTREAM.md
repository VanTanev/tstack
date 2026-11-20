# Upstream

`SKILL.md` is a skill of this repo.
Its "Round 1 code review" section has a changed copy of the Standards and Spec reviews of Matt Pocock's `code-review` skill, so that `sol-loop` does not depend on another skill.

## `code-review`

- Repository: https://github.com/mattpocock/skills, branch `main`, file `skills/engineering/code-review/SKILL.md`.
- Base: `7739eaed7f8f3915437a8def198a6d0d7206dbc7` (2026-10-29, "Start subagents with a fresh context window, not a fork"), the last change to the file or to `LICENSE`.
- Copied: the spec search of step 2, the standards search and the smell baseline of step 3, and the two sub-agent prompts of step 4.
- Changed: the smell lines are shorter. The prompts are Sol briefs with severities and stable ids. The code review never asks the user, and its steps 1, 4 (foreground sub-agents) and 5 (aggregate report) are left out, because `sol-loop` has its own scope, reviewers and ledger.
- License: the MIT notice in `LICENSE`.

## Update procedure

1. In an up-to-date clone of https://github.com/mattpocock/skills, run `git diff <base>..origin/main -- skills/engineering/code-review/SKILL.md LICENSE`.
   If the diff is empty, stop.
2. Otherwise, port the changes to the copied parts into the "Round 1 code review" section by hand.
   If the license changed, copy its new text into `LICENSE`.
   Set "Base" to the last commit that changed the file or `LICENSE`.
