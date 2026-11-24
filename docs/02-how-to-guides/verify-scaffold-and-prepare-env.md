# How to Verify the Scaffold and Local Ignore Rules

Use this procedure to verify repository integrity and protect local environment files.

## Prerequisites

- Confirm Git is installed on the host.
- Confirm Python 3 is installed on the host.

NOTE: Review tracked files and ignore patterns in [Repository Files and .gitignore Reference](../03-reference/repository-files-and-gitignore.md).

## Procedure

### Verify Tracked Files and Ignore Rules

CAUTION: Keep `.env` inside `.gitignore` before you store local variables. Committed `.env` files leak secrets in Git history.

1. List tracked repository files from the root directory:

```bash
git ls-files
```

2. Confirm that Git ignores `.env` and Go binary extensions:

```bash
git check-ignore -v .env demo.exe coverage.out
```

3. Run the automated verification suite:

```bash
python3 -m unittest discover -s tests -p "test_*.py" -v
```

## Validation

Confirm the test suite exits cleanly and Git reports a clean repository status:

```bash
git status --short
```

## Rollback

If a local test creates temporary `.env` or cache files, delete them safely:

```bash
rm -f .env
```

Read project baseline context in [Prototype Baseline and Planned Design](../04-explanation/prototype-baseline-and-planned-design.md).
