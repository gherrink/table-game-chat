# TableGameChat
Experiment to create chatbot to explain and help with table games.

## Install

### Local

```
python3 -m venv --prompt venv .venv
source .venv/bin/activate
pip install -e .[dev]
```


## Commands

- `tox` - Run all
- `tox run -e lint` - Run linter
- `tox run -f test` - Run tests
- `tox run -e docs` - Build documentation
- `tox run -e build` - Build package


## Tools & Libraries

- `tox` - Automation of tests, linters, etc. - https://tox.wiki/
- `pytest` - Testing framework - https://docs.pytest.org/en/stable/
- `ruff` - Linter - https://docs.astral.sh/ruff/
- `sphinx` - Documentation - https://www.sphinx-doc.org/en/master/


## Sources

- Project setup: https://medium.com/@Mr_Pepe/setting-your-python-project-up-for-success-in-2024-365e53f7f31e & https://github.com/Mr-Pepe/python-template/