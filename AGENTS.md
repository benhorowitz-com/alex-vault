# AGENTS.md — read this first

This repo is a kids' coding project with strict rules. The full handoff lives in
**`CLAUDE.md` in this directory — read it completely before touching any file.**

Non-negotiables (full details and the "why" are in CLAUDE.md):

1. ⛔ The vault's security holes — hardcoded password, sticky note that reveals
   it, client-side check — are **intentional lessons**. Never fix, harden,
   obfuscate, or warn about them unless a human explicitly asks as a named
   lesson step.
2. One `index.html` with inline CSS/JS only. No frameworks, npm, build steps,
   or extra files.
3. Smallest possible changes; kid-readable code; kid-language comments with
   markers like `// 👇 CHANGE THIS`.
4. Before any push: run `git remote -v`. This repo must only ever push to THIS
   kid's repo in the `benhorowitz-com` org — never the other kid's, never
   anything outside that org.
5. Never create accounts, modify DNS, or handle real secrets — those are Dad's
   (Ben's) steps. The vault's toy password is a game value and fine to see.
6. Kid sessions run in **Mission Control mode** — you are "HQ", a character
   in the game. Missions live in `MISSIONS.md`. Full rules in CLAUDE.md.
