# Repository Files and `.gitignore` Reference

Exact inventory of files, ignore patterns, and unimplemented scope in the **GTAnsible** `v0.1.0` repository.

## Committed Artifacts

| Path | Size / Scope | Specification |
| :--- | :--- | :--- |
| `README.md` | Markdown | Project overview, current prototype status disclosure, conceptual Mermaid diagram, and test command |
| `LICENSE` | `674` lines | GNU General Public License Version 3 (`29 June 2007`) |
| `.gitignore` | `37` lines | GitHub Go deny-list template plus `__pycache__/` and `*.pyc` rules |
| `docs/` | Markdown portal | Four Diátaxis quadrants (`01-tutorials`, `02-how-to-guides`, `03-reference`, `04-explanation`) |
| `tests/test_docs_tutorials_howtos.py` | Python `unittest` | Automated validation of scaffold files, `.gitignore` rules, Diátaxis, STE, links, and Mermaid |

## `.gitignore` Rule Categories

| Category | Patterns | Purpose |
| :--- | :--- | :--- |
| Binaries & shared libraries | `*.exe`, `*.exe~`, `*.dll`, `*.so`, `*.dylib` | Prevents committing compiled Go binaries |
| Test & coverage outputs | `*.test`, `*.out`, `coverage.*`, `*.coverprofile`, `profile.cov` | Ignores `go test -c` binaries and coverage profiles |
| Workspace & environment | `go.work`, `go.work.sum`, `.env` | Keeps local Go workspace overrides and secrets untracked |
| Python test cache | `__pycache__/`, `*.pyc` | Prevents Python bytecode pollution when running `unittest` |

## Unimplemented Scope (`v0.1.0`)

| Component | Repository State |
| :--- | :--- |
| Go module & backend (`go.mod`, `*.go`) | Absent — not yet created |
| Web frontend assets (HTML/CSS/JS) | Absent — not yet created |
| Ansible playbooks & inventories | Absent — not yet created |
| CI/CD workflows (`.github/workflows/`) | Absent — not yet created |
