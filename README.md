# Python project template

Authors:

Explain what the project is about and any other things users may need to know.

## Project setup and management with uv
https://docs.astral.sh/uv/

### Install uv
```bash
curl -LsSf https://astral.sh/uv/0.12.12/install.sh | sh
```
Update with `uv self update`

### Sync (install) project dependencies
```bash
uv sync
```
If the project is version controlled, it is important to add the poetry.lock file to the project repository.

Add dependencies using `uv add packagename`

For compatibility with other tools, one can export the uv.lock to pylock.toml

## Pyrefly type checker / language server
https://pyrefly.org/en/docs/

Pyrefly is used as the language server and type checker.
It is part of the `dev` dependency group, which is synced to the workspace by default.

You can just install the VSCode extension and/or use it in terminal:
```bash
pyrefly check --summarize-errors # runs Pyrefly and gives a summary of type errors
```

## Ruff formatter / linter
https://docs.astral.sh/ruff/

Ruff is the used formatter and linter in this project (also part of `dev`).
It can be installed as a VSCode extension and/or used in the command line
```bash
uv run ruff check   # Lint all files in the current directory.
uv run ruff format  # Format all files in the current directory.
```