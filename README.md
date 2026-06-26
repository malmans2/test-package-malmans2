# test-package-malmans2

[![Static Badge](https://github.com/ecmwf/codex/raw/refs/heads/main/Project%20Maturity/emerging_badge.svg)](https://github.com/ecmwf/codex/raw/refs/heads/main/Project%20Maturity#emerging)

Test package malmans2

> [!IMPORTANT]
> This software is **Emerging** and subject to ECMWF's guidelines on [Software Maturity](https://github.com/ecmwf/codex/raw/refs/heads/main/Project%20Maturity).

## Quick Start

```python
>>> import test_package_malmans2

```

> [!NOTE]
> All Python code examples in this README are automatically tested as part of the unit test suite.

## Developer Workflow

### 1. Initialise the Repository

Create a repository on GitHub under the ecmwf organisation named test-package-malmans2. Then, run:

```bash
git init -b main
git add .
git commit -m "initialise repository"
git remote add origin git@github.com:ecmwf/test-package-malmans2.git
git push -u origin main
```

### 2. Set Up the Environment

Configure your virtual environment and pre-commit hooks:

```bash
make install
```

> [!NOTE]
> This project uses uv for dependency management. Commit the generated uv.lock file to version control.

### 3. Run Quality Assurance

Check formatting, linting, and lockfile consistency:

```bash
make qa
```

### 4. Commit and Push

Save and push any automatically formatted changes:

```bash
git add .
git commit -m "format codebase and sync lockfile"
git push origin main
```

The CI/CD pipeline triggers on pull requests, merges to main, and new releases.

## Useful Makefile Targets

All development tasks are configured as self-documenting targets in the Makefile. To see a complete list of available targets and their descriptions, run:

```bash
make help
```

This will output a clean list of all available utility commands, including:

- Environment setup: `make install`
- Quality assurance checks: `make qa`
- Unit tests: `make unit-tests`
- Type checking: `make type-check`

To run all quality checks, tests, and build steps in a single sequence, use the shortcut:

```bash
make all
```

## Instructions for PyPI

Publishing to PyPI is done using a Trusted Publisher. See the [PyPI documentation](https://docs.pypi.org/trusted-publishers/adding-a-publisher/).
Configure the Trusted Publisher with the following settings:

- **Owner**: `ecmwf`
- **Repository name**: `test-package-malmans2`
- **Workflow name**: `on-release.yml`
- **Environment name**: `pypi`

## Instructions for GitHub Pages

1. Go to **Settings → Pages**, then set **Source** to **GitHub Actions**.
1. Go to **Settings → Environments → GitHub Pages**, then add a deployment tag rule with the name pattern `"v*"`.

## License

```
Copyright 2026, Mattia Almansi.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```
