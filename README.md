# 🔐 Agent Alex's Secret Vault

Live at **https://alexhorowitz.me** · part of the family Agent HQ game.
One file (`index.html`), no build steps, no frameworks. The AI agent in this
repo plays **HQ — Mission Control**; the missions live in `MISSIONS.md`.

> **Agents: read `CLAUDE.md` in this repo FULLY before touching anything.**
> It is the rulebook. `AGENTS.md` is the short version for Codex.

## New computer? Agent setup runbook

You are an agent setting up this vault on Agent Alex's own computer. Work the
checklist top to bottom. Anything involving passwords or logins is **Dad's
(Ben's) step** — if auth is missing or wrong, stop and hand the keyboard to
Ben. Never enter or store credentials yourself.

1. **Tools check** — `git`, `gh`, and `claude` (or `codex`) must all be on
   PATH. Anything missing? Tell Ben exactly what to install and stop there.
2. **Right account** — run `gh auth status`. It must show **`aphorowitz`**.
   Any other account (especially an adult's) → STOP and have Ben run
   `gh auth login` as `aphorowitz`.
3. **Clone** (skip if you're already inside a local copy):
   `gh repo clone benhorowitz-com/alex-vault && cd alex-vault`
4. **Identity** — commits must carry the kid's own name, set repo-local:
   ```sh
   git config user.name  "aphorowitz"
   git config user.email "aphorowitz@users.noreply.github.com"
   ```
5. **Remote check** — `git remote -v` must point at
   `benhorowitz-com/alex-vault` and nothing else.
6. **Trust** — the first interactive `claude` run in this folder shows a
   trust prompt. Ben accepts it once; that activates
   `.claude/settings.json` (pre-approved read-only git commands — commit and
   push stay behind prompts on purpose; that's the ritual).
7. **Smoke test** — all three must pass:
   - `git pull` → clean
   - `git push --dry-run` → succeeds (a 403 means the wrong account is
     logged in — back to step 2)
   - `open index.html` → the vault door appears
8. **Handover** — greet the kid as HQ and offer Mission 1 or mission
   roulette. From then on they just double-click `START-MISSION.command`.

## Troubleshooting

| Symptom | Fix |
|---|---|
| Push rejected (403) | Wrong GitHub account is logged in — get Ben (step 2) |
| "Your branch is behind" | `git pull` — a session on another computer pushed |
| The page is broken | Panic button: restore the last save point (rules in `CLAUDE.md`) |
| Site not updating after push | GitHub Pages takes ~1 min; hard-refresh the browser |
