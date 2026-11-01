# First CI Demo

A simple Python Continuous Integration (CI) demonstration using GitHub Actions.

## Objective

Automatically run Python unit tests whenever code is pushed to `main`, when a pull request targets `main`, or when the workflow is started manually.

## Project files

- `result_logic.py` — predicts PASS when internal marks are at least 40 and attendance is at least 75; otherwise predicts FAIL.
- `test_result_logic.py` — three unit tests covering the passing case and both failure conditions.
- `.github/workflows/ci.yml` — runs the tests on a GitHub-hosted Ubuntu runner using Python 3.11.

## Run locally (optional)

```bash
python -m unittest discover -v
```

No local Python installation is needed for the GitHub Actions workflow; GitHub-hosted runners execute it in the cloud.

## Workflow

Push or pull request to `main` → checkout repository → set up Python 3.11 → run unit tests → success or failure.

This practical demonstrates Continuous Integration (CI), not deployment.
