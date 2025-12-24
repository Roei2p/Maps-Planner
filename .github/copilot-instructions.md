# GitHub Copilot Instructions for Maps-Planner

Purpose
- Help AI coding agents be immediately productive in this repository by describing the current code state, discovered conventions (if any), and safe first actions.

Quick repo summary (discoverable facts)
- The repository currently only contains `README.md` which references "Built with AI Studio" and Gemini.
- There are **no** source files, no tests, and no CI configuration in the repo at this time.

Primary guidance for AI agents
- DO NOT make large unstated assumptions (language, frameworks, CI, target platform).
- Before introducing major structure or code, **ask the maintainers** the exact decisions listed below and open an Issue if no answer is given.

High-value first actions (safe, discoverable)
1. Create an Issue titled: **"Project scaffold: propose language, layout, and CI"** with a short checklist and proposed options (Python/Node, `src/` + `tests/`, GitHub Actions sample).
2. If maintainers prefer an initial scaffold and have given permission in the Issue, create a small, well-scoped PR that:
   - Adds a `src/` directory and a minimal project entry point (`src/main.py` or `src/index.js`).
   - Adds a `tests/` directory with a single smoke test that fails until functionality is implemented.
   - Adds a basic GitHub Actions workflow that runs lint and tests on push to `main`.
3. Update `README.md` to include the selected language, build/test commands and a short development quick-start section.

Questions to ask maintainers (copy into Issues/PR descriptions)
- Which programming language(s) should we use for implementation? (e.g., Python 3.11, Node 18)
- Which test framework do you prefer? (e.g., `pytest`, `jest`)
- Preferred lint/format tools? (e.g., `black`/`ruff`, `prettier`/`eslint`)
- Do you want GitHub Actions as CI? Any required matrix (multiple runtimes)?
- Any existing architecture or constraints not in the repo (hosting, license, integration points)?

Project-specific conventions and patterns
- None are discoverable from the current files. Record any conventions provided by maintainers back into this file so future agents can follow them.

PR & commit rules (project-specific safe defaults)
- Keep PRs small and focused (one feature/refactor per PR).
- Include a short summary of the change, the motivation, and how to test locally.
- Include at least one smoke test for new functionality.

Example PR description template
- Summary: one-line
- Motivation: why this change is needed
- Changes: bullet list of files added/modified
- How to test: commands to run locally
- Checklist: tests added, linter passes, changelog updated (if applicable)

When you don't know: open an Issue
- If any design question is unanswered, open an Issue summarizing the options and recommended choice; wait for a maintainer to reply before wide-reaching changes.

Where to record new conventions
- Add them to `.github/copilot-instructions.md` and to `README.md` so they are visible to human contributors.

If you are blocked
- Add a short comment to the blocking Issue indicating what information is needed (assign to repo owners if possible).

Contact & context
- If a maintainer username is referenced anywhere in issues/PRs, prefer direct mention to get faster clarification.

---

If you want, I can now scaffold a minimal Python or Node starter (small PR + CI + smoke test) — tell me which language to propose in the Issue or I can open the Issue for you to confirm.