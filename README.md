=== README.md ===
# Python • L2C Workspace

This repo is my **hands-on Python workspace** for the *Learn to Cloud (L2C)* path (Phase 2: Programming).
Goal: get practical with Python for **automation, APIs, storage/DB, testing**, then ship a small **capstone API**
I can later deploy in the cloud.

> Owner: **Ilyas El-Hallaoui** (GitHub: `Ilyos-creater`)

---

## Why this repo?
- Keep all **notes, labs, and mini-projects** in one place.
- Build a repeatable **tooling baseline** (venv, lint, tests).
- Prepare for the L2C **capstone** (journal/notes API) and a later **cloud deploy**.

---

## What I’m doing here
1. **Python basics** – syntax, types, functions, modules, error handling.
2. **Automation & APIs** – file I/O, JSON/CSV, HTTP clients, small scripts.
3. **Storage** – quick persistence with SQLite.
4. **Web/API** – FastAPI + tests.
5. **Capstone** – refactor/extend a small Journal/Notes API, add tests & CI, containerize.

---

## Stack & Conventions
- **Python** 3.12 (venv)
- **Tooling**: `black` (format), `ruff` (lint), `pytest` (tests)
- **HTTP**: `requests` / `httpx`
- **API**: `fastapi` + `uvicorn`
- **DB (simple)**: `sqlmodel` / SQLite
- **Env/Config**: `python-dotenv`

**Layout**
    .
    ├─ src/            # code
    │  ├─ main.py
    │  └─ api.py       # added when FastAPI starts
    ├─ tests/          # pytest tests
    ├─ .venv/          # virtual env (ignored)
    ├─ .gitignore
    ├─ pyproject.toml  # black/ruff config
    └─ README.md

---

## Getting started (WSL/Ubuntu)

~~~bash
# clone (SSH)
git clone git@github.com:Ilyos-creater/l2c-python.git
cd l2c-python

# venv
python -m venv .venv
source .venv/bin/activate
python -m pip install --upgrade pip

# base tooling & libs
pip install black ruff pytest requests python-dotenv fastapi "uvicorn[standard]" httpx sqlmodel
~~~

**Quality checks**
~~~bash
pytest -q
ruff check .
black --check .
~~~

---

## Tiny API (when present)

~~~bash
uvicorn src.api:app --reload
# http://127.0.0.1:8000/health  -> {"status":"ok"}
~~~

---

## Dev tips
- Work inside WSL **Linux path** (e.g. `~/code/...`) to avoid slow I/O.
- Use **SSH keys** for GitHub (ed25519, loaded via ssh-agent).
- Commit small, push before switching machines: `git push` here → `git pull` there.

---

## Roadmap
- [ ] Week 1–2: Python fundamentals + small CLI scripts (logs, JSON, CSV).
- [ ] Week 3: SQLite quick-store + search; logging & `.env`.
- [ ] Week 4: Spin up **FastAPI** with tests (CRUD + health).
- [ ] Week 5: Start **Capstone** (journal/notes API): refactor, type hints, tests.
- [ ] Week 6: Add features, **CI (GitHub Actions)**, container image, release notes.
- [ ] Phase 3 (later, L2C): **Deploy** (container/VM, networking, secrets, monitoring).

---

## L2C reference
This repo follows the *Learn to Cloud (L2C) – Programming (Python)* focus:
scripting, APIs, storage, testing, and a small API capstone to deploy in the cloud.
I’m starting with a free playlist/course; if I hit gaps, I’ll add a lightweight book/reference.

---

## License
Personal learning repo. Feel free to peek and adapt snippets; no warranty.

---

### Contact
- GitHub: `Ilyos-creater`
