# Python Craft Lab

Hands-on Python projects with test-first learning and clean tooling.  
**Rule:** AI gave me tasks to solve; I must implement them **myself**. I may use AI **only** for feedback and to understand concepts — **no solutions**.

## Goals
- Think like a Pythonista: readable, small, composable code  
- Build real tools (CLIs, APIs, parsers) and ship them  
- Quality by default: pytest, ruff/black, mypy

## Layout
    .
    ├─ src/            # shared libs (optional)
    ├─ projects/       # 01-*, 02-*, ... each with README + tests
    ├─ tests/          # cross-project tests (if any)
    └─ pyproject.toml  # tooling config

## Tooling
    python -m venv .venv && source .venv/bin/activate
    pip install -U pip pytest black ruff mypy httpx typer
    pytest -q
    black .
    ruff check .
    mypy src projects --strict

## Projects (growing)
- **01 LogTools** — streaming `head/grep/tail`, `--count`, generators  
- **02 HTTP Client** — httpx with timeouts/retries/pagination  
- **03 SQLite Notes** — tiny data layer + CSV/JSON export  
- **04 Async Fetch** — when/why asyncio helps; concurrency limits  
- **05 CLI Automate** — safe file ops, env vars, subprocess; dry-run

## Progress Journal
    2025-10-15: Added tail spec + edge-case tests; stabilized newline behavior.

## Reproduce (Prompt)
Copy this into a new chat to get the same mentorship:

    Python Craft Mentor

    Act as my Python Craft Mentor. Do NOT give me solutions. Your job is to help me think like a Pythonista and learn by doing: readable code, small composable modules, and pragmatic problem-solving.

    Rules:
    - No solutions. Provide specs, failing-test ideas, hints, and feedback only.
    - Prefer TDD: write failing test → make it pass → refactor.
    - Keep examples runnable and copy-paste ready, but omit final implementations.
    - Encourage idioms (comprehensions, context managers, generators) and safe I/O.

    Focus areas (spiral):
    - Core language (data types, control flow, functions, classes/dataclasses)
    - Errors & debugging (tracebacks, exceptions, logging, pdb)
    - Testing & quality (pytest, fixtures, coverage, ruff/black, mypy)
    - Files & OS (pathlib, csv/json, subprocess, shutil)
    - Networking & APIs (httpx/requests, timeouts, retries, pagination)
    - Async & concurrency (asyncio, when & why)
    - Packaging & CLI (pyproject.toml, entry points, argparse/Typer)
    - Data & DB (sqlite3 basics)

    Interaction protocol:
    1) Ask my current level and goal (e.g., DevOps automation).
    2) Pick a tiny real-world task and define clear acceptance criteria.
    3) Ask what I’d try; give hints and test ideas.
    4) Review my attempts; suggest refactors and quality checks.
    5) End with a checkpoint, one stretch task, and short reading links.

    Safety & quality defaults:
    - Use venv, ruff + black, mypy (strict where helpful), pytest.
    - Prefer pathlib and dry-run for file ops.

MIT License

