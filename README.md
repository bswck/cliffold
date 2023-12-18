
# cliffold [![Package version](https://img.shields.io/pypi/v/cliffold?label=PyPI)](https://pypi.org/project/cliffold/) [![Supported Python versions](https://img.shields.io/pypi/pyversions/cliffold.svg?logo=python&label=Python)](https://pypi.org/project/cliffold/)
[![Tests](https://github.com/bswck/cliffold/actions/workflows/test.yml/badge.svg)](https://github.com/bswck/cliffold/actions/workflows/test.yml)
[![Coverage](https://coverage-badge.samuelcolvin.workers.dev/bswck/cliffold.svg)](https://coverage-badge.samuelcolvin.workers.dev/redirect/bswck/cliffold)
[![Poetry](https://img.shields.io/endpoint?url=https://python-poetry.org/badge/v0.json)](https://python-poetry.org/)
[![Ruff](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/astral-sh/ruff/main/assets/badge/v2.json)](https://github.com/astral-sh/ruff)
[![Code style](https://img.shields.io/badge/code%20style-black-000000.svg?label=Code%20style)](https://github.com/psf/black)
[![License](https://img.shields.io/github/license/bswck/cliffold.svg?label=License)](https://github.com/bswck/cliffold/blob/HEAD/LICENSE)
[![Pre-commit](https://img.shields.io/badge/pre--commit-enabled-brightgreen?logo=pre-commit&logoColor=white)](https://github.com/pre-commit/pre-commit)

Analyze `--help` outputs of CLIs to generate programmatic client libraries.

# The idea

1. `cliffold scaffold-cli-lib git --dest=cliffold/git`
2. Thanks to `--help` output, cliffold generates a Python library that can be used to interact with the CLI:
```py
from cliffold.git import Git

git = Git()
print(git.version)
git.init()
git.commit(message="Initial commit")
```

To make this possible, `cliffold` is currently in its research and collects CLI outputs.
Feel free to submit your CLI propositions with installation methods in [#1](https://github.com/bswck/cliffold/issues/1).
See [cliffold_research.md](https://github.com/bswck/cliffold/blob/HEAD/cliffold_research.md) to check out the current research results.

# Installation



You might simply install it with pip:

```shell
pip install cliffold
```

If you use [Poetry](https://python-poetry.org/), then run:

```shell
poetry add cliffold
```

## For contributors

<!--
This section was generated from bswck/skeleton@01e08d2.
Instead of changing this particular file, you might want to alter the template:
https://github.com/bswck/skeleton/tree/01e08d2/fragments/guide.md
-->

> [!Note]
> If you use Windows, it is highly recommended to complete the installation in the way presented below through [WSL2](https://learn.microsoft.com/en-us/windows/wsl/install).



1.  Fork the [cliffold repository](https://github.com/bswck/cliffold) on GitHub.

1.  [Install Poetry](https://python-poetry.org/docs/#installation).<br/>
    Poetry is an amazing tool for managing dependencies & virtual environments, building packages and publishing them.
    You might use [pipx](https://github.com/pypa/pipx#readme) to install it globally (recommended):

    ```shell
    pipx install poetry
    ```

    <sub>If you encounter any problems, refer to [the official documentation](https://python-poetry.org/docs/#installation) for the most up-to-date installation instructions.</sub>

    Be sure to have Python 3.8 installed—if you use [pyenv](https://github.com/pyenv/pyenv#readme), simply run:

    ```shell
    pyenv install 3.8
    ```

1.  Clone your fork locally and install dependencies.

    ```shell
    git clone https://github.com/your-username/cliffold path/to/cliffold
    cd path/to/cliffold
    poetry env use $(cat .python-version)
    poetry install
    ```

    Next up, simply activate the virtual environment and install pre-commit hooks:

    ```shell
    poetry shell
    pre-commit install --hook-type pre-commit --hook-type pre-push
    ```

For more information on how to contribute, check out [CONTRIBUTING.md](https://github.com/bswck/cliffold/blob/HEAD/CONTRIBUTING.md).<br/>
Always happy to accept contributions! ❤️


# Legal info
© Copyright by Bartosz Sławecki ([@bswck](https://github.com/bswck)).
<br />This software is licensed under the terms of [MIT License](https://github.com/bswck/cliffold/blob/HEAD/LICENSE).
