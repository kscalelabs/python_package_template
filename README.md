# Using this template

After creating a new repository from this template, update the following items before adding your code.

## Pick your project details
- Distribution name (project/PyPI name), e.g., "my-package"
- Python package import name (directory name), e.g., "my_package"
- Short description
- Project URL (e.g., GitHub repo URL)
- Author name and email
- Minimum supported Python version (e.g., 3.11)
- Copyright year

## Rename the package directory
- Rename the directory `template_package/` to your chosen Python import name (e.g., `my_package/`).

## Edit these files
- `setup.py`:
  - `name`: set to your distribution/project name.
  - `description`: set a short description.
  - `author`: set your name.
  - `url`: set your project URL.
  - `python_requires`: set your minimum Python version (e.g., ">=3.11").
  - Update file paths that reference the package directory so they point to your renamed package (lines that open `template_package/requirements.txt` and `template_package/__init__.py`).
  - Optional: add `author_email`, `classifiers`, and console `entry_points` if you need a CLI.

- `pyproject.toml`:
  - `[tool.ruff] target-version`: set to your target (e.g., `py311`).
  - `[tool.ruff.lint.isort] known-first-party`: replace `template_package` with your package import name.

- `MANIFEST.in`:
  - Replace `template_package/` with your package directory so included files are packaged correctly.

- `Makefile`:
  - The help text shows the project name and Python version; update both to match your choices.

- `LICENSE`:
  - Update the year and author name.

- `.github/workflows/test.yml` and `.github/workflows/publish.yml`:
  - Update the `python-version` to your chosen minimum.
  - Optional: change the default branch name in triggers if your repo uses `main` instead of `master`.

- `README.md` (this file):
  - Replace the title and content with your project documentation.

- `<your_package>/__init__.py`:
  - Set `__version__` to your starting version (e.g., `0.1.0`).

- `<your_package>/requirements.txt`:
  - List your runtime dependencies (one per line). Dev tools are already configured in `setup.py` under the `dev` extra.

## Start coding
- Place your source code inside the renamed package directory.
- Tests live under `tests/`. Adjust or extend as needed.
