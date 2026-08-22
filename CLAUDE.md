# CLAUDE.md

Guidance for Claude Code (and other AI assistants) working in this repository.

## What this repository is

This is `PrivSter/PrivSter` — a GitHub **profile README repo**. GitHub gives
every account the option to create a repo matching their username; its
`README.md` is then rendered on the user's public profile page instead of
being a normal project README. This repo is that special case, not an
application, library, or course project.

There is effectively no "codebase" here:

- `README.md` — the content shown on https://github.com/PrivSter. It's a
  short bio (interests: scripting, Python, cybersecurity; currently
  learning basic scripting and Linux).
- `Temprogram` — a small standalone Bash script, unrelated to the profile
  README, that appends a Raspberry Pi CPU temperature reading to
  `~/Desktop/readings.txt` via `vcgencmd measure_temp` (Raspberry Pi OS
  only — `vcgencmd` isn't available on other platforms).

## Working conventions

- Treat `README.md` edits as profile-bio copy edits, not documentation for
  a project — keep changes to tone/content the user actually wants shown
  publicly, and preserve the GitHub-generated HTML comment block explaining
  what the file is.
- `Temprogram` is a personal utility script, not part of any larger system.
  If asked to modify or extend it, keep it a simple, dependency-free Bash
  script; don't wrap it in project scaffolding (no package manager, tests,
  or CI) unless explicitly requested.
- This repo has no build step, no dependencies, and no test suite. There is
  nothing to install or run except invoking `Temprogram` directly on a
  Raspberry Pi (`sudo vcgencmd` requires the `vcgencmd` tool from
  `libraspberrypi-bin`, present by default on Raspberry Pi OS).
- Given the tiny size and personal nature of this repo, avoid introducing
  new structure (directories, configs, frameworks) unless the user asks for
  it — the goal is targeted, minimal edits, not scaffolding a project.
