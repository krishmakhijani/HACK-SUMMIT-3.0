# Contributing

As an open source project,  welcomes contributions of all forms. If you would like to bring the project
forward, please consider contributing in the following areas:

- **Maintenance:** We are *incredibly* thankful for individuals who are stepping up and helping with maintenance. This
  includes (but is not limited to) triaging issues, reviewing pull requests and picking up stale ones, helping out other
  users on [GitHub Discussions], creating minimal, complete and
  verifiable examples or test cases for existing bug reports, updating documentation, or fixing minor bugs that have
  recently been reported.

## Development Setup

To get started h, please install a recent version of Python (we require at least Python 3.9).
Then, do the following:

##### Linux / macOS

```shell
# 1) Verify that these commands work:
python3 --version
python3 -m pip --help
python3 -m venv --help
# 2) Install:
git clone https://github.com/krishmakhijani/HACK-SUMMIT-3.0
cd HACK-SUMMIT-3.0
python3 -m venv venv
venv/bin/pip install -e ".[dev]"
```

##### Windows

```shell
# 1) Verify that this command works:
python --version
# 2) Install:
git clone https://github.com/krishmakhijani/HACK-SUMMIT-3.0
cd HACK-SUMMIT-3.0
python -m venv venv
venv\Scripts\pip install -e .[dev]
```

This will clone  source code into a directory with the same name,
and then create an isolated Python environment (a [virtualenv](https://virtualenv.pypa.io/)) into which all dependencies are installed.
itself is installed as "editable", so any changes to the source in the repository will be reflected live in the virtualenv.

The main executables for the project – ` – are all created within the virtualenv.
After activating the virtualenv, they will be on your $PATH, and you can run them like any other command:

##### Linux / macOS

```shell
source venv/bin/activate
django --version
```

##### Windows

```shell
venv\Scripts\activate
django --version
```

## Testing

If you've followed the procedure above, you already have all the development requirements installed, and you can run the
basic test suite with [tox](https://tox.readthedocs.io/):

```shell
tox -e py      # runs Python tests
```

Our CI system has additional tox environments that are run on every pull request (see [tox.ini](./tox.ini)).

For speedier testing, you can also run [pytest](http://pytest.org/) directly on individual test files or folders:



Please ensure that all patches are accompanied by matching changes in the test suite. The project tries to maintain 100%
test coverage and enforces this strictly for some parts of the codebase.

### Code Style

Keeping to a consistent code style throughout the project makes it easier to contribute and collaborate.

We enforce the following check for all PRs:

```shell
tox -e flake8
```

If a linting error is detected, the automated pull request checks will fail and block merging.

## Documentation

Please check [docs/README.md](./docs/README.md) for instructions.
