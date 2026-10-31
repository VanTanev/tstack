# Upstream

`SKILL.md` is a skill of this repo.
Its `references/` has a copy of the user-invoked `no-comments` skill, because step 3 runs it and a skill cannot start a user-invoked skill.
Each file is a byte copy of its source at the base below.

## `no-comments`

- Repository: https://github.com/VanTanev/skills, branch `main`.
  Its `skills/no-comments/` is a changed copy of pstack `no-comments` from https://github.com/cursor/plugins, and its `UPSTREAM.md` lists the changes.
- Paths: `skills/no-comments/SKILL.md` is `references/no-comments.md`, and `skills/no-comments/references/comment-sicko.md` is `references/comment-sicko.md`.
- Base: `2257f9768971772efec8e5161295287310a3cffd` (2026-10-29, "Start subagents with a fresh context window, and port Matt's build and tracker fixes"), the last change to these files.
- License: the pstack notice in `LICENSE`.

## Update procedure

1. In an up-to-date clone of https://github.com/VanTanev/skills, run `git diff <base>..origin/main -- skills/no-comments/SKILL.md skills/no-comments/references/comment-sicko.md skills/no-comments/LICENSE`.
   If the diff is empty, stop.
2. Otherwise, run `git -C <clone> show origin/main:skills/no-comments/SKILL.md > references/no-comments.md` and `git -C <clone> show origin/main:skills/no-comments/references/comment-sicko.md > references/comment-sicko.md`.
   If the license changed, copy its new text into `LICENSE`.
   Set "Base" to the last commit that changed these files.
