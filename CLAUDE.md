# Research Lab — working conventions

This is a daily research workspace shared between simsam and Claude. We explore
topics, run small experiments, and recreate published papers to understand them.

## Layout

- `journal/<year>/<YYYY-MM-DD>.md` — daily lab notebook entry
- `topics/<topic-name>/` — notes + small code for learning a topic (copy `topics/_template/`)
- `papers/<short-paper-name>/` — one paper recreation per folder (copy `papers/_template/`)
- `projects/<project-name>/` — standalone mini-projects

## Rules for every session

1. **End each session with a journal entry** in `journal/<year>/<YYYY-MM-DD>.md`:
   what we explored, what we learned, what's still open. Append if the file exists.
2. **Update the Index section of the root README** when a new paper/topic/project
   folder is created or completed.
3. **New paper recreation**: copy `papers/_template/` to `papers/<short-name>/`
   (e.g. `papers/attention-is-all-you-need/`), fill in the README before coding.
4. **Python environments**: use `uv` per-folder (`uv init` / `uv run`) so each
   paper/project pins its own dependencies. Never install into system Python.
5. **Commits**: small and frequent, message format `<area>: <what>` —
   e.g. `papers/lora: add rank-ablation experiment`, `journal: 2026-07-30`.
6. **Datasets and large files** stay out of git — download scripts or links in
   the folder README instead. `data/` directories are gitignored everywhere.
7. **Installs, new skills, or MCP servers**: propose to simsam first and wait
   for approval before installing.
