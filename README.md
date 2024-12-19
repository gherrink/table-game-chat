# TableGameChat
Experiment to create chatbot to explain and help with table games.

## Install

### Local

```
python3 -m venv --prompt venv .venv
source .venv/bin/activate
pip install -e .[dev]
gitlint install-hook
```

To automatically sign-off your commits, you can create the following command under `~/.git/hooks/prepare-commit-msg`:

```shell
#!/bin/sh

# https://stackoverflow.com/questions/15015894/git-add-signed-off-by-line-using-format-signoff-not-working/46536244#46536244

NAME=$(git config user.name)
EMAIL=$(git config user.email)

if [ -z "$NAME" ]; then
    echo "empty git config user.name"
    exit 1
fi

if [ -z "$EMAIL" ]; then
    echo "empty git config user.email"
    exit 1
fi

# add signed-off-by to git commit msg
git interpret-trailers --if-exists doNothing --trailer \
    "Signed-off-by: $NAME <$EMAIL>" \
    --in-place "$1"
```

Don't forget to make the file executable:

```shell
chmod +x ~/.git/hooks/prepare-commit-msg
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
- `gitlint` - Linter git commits with conventional commits  - https://jorisroovers.com/gitlint/latest/rules/contrib_rules/#ct1-contrib-title-conventional-commits



## Sources

- Project setup: https://medium.com/@Mr_Pepe/setting-your-python-project-up-for-success-in-2024-365e53f7f31e & https://github.com/Mr-Pepe/python-template/