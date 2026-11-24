# github-actions-learning

![CI Pipeline](https://github.com/knawazia/github-actions-learning/actions/workflows/ci.yml/badge.svg)

A tiny Python calculator used to learn GitHub Actions.

## CI pipeline

Every push and pull request to `main` runs:

1. **Lint** – `ruff check .`
2. **Test** – `pytest` with coverage on Python 3.10, 3.11 and 3.12 (in parallel)
3. **Build** – `python -m build`, uploaded as a downloadable artifact

## Run locally

```bash
pip install -r requirements.txt
ruff check .
pytest -v --cov=app
python -m build
```