# re-python-package

This template repository is created by the [UU Research Engineering team](https://utrechtuniversity.github.io/research-engineering/) and is aimed to provide a simple project template for python package development.

The template includes:
- Project directory structure
- Project configuration using `pyproject.toml`
- GitHub actions workflows for testing, linting, type checking and publishing on pypi

Many other project templates exist, check for example this advanced [python template](https://github.com/NLeSC/python-template) by the NL eScience Center.

## Dependencies
This template uses:
| Tool | Aim |
| --- | --- |
| setuptools | building |
| flake8, pylint | code linting |
| pytest | testing |
| pydocstyle | checking docstrings |
| mypy | type checking |
| sphinx | documentation generation |

If needed, most of these tools can be removed by simply removing the GitHub action that calls the tool, or by changing `pyproject.toml`

## How to use

### Step 1: Create new repository from this template
Click `Use this template` at the top of this page to create a new repository using this template

### Step 2: Change the name of your package in pyproject.toml
- Change the name of the folder `packagename` to the name of your package
- Open `pyproject.toml` and change `packagename` to the name of your package
- Also change the authors and optionally any other items that you want to change

### Step 3: Change GitHub Actions workflow
- Open `.github/workflows/python-package.yml`
- Change `packagename` to the name of your package (line 21)
- Many actions are commented out, uncomment them when you want to start using them.

### Step 4: Replace this README file with your README
- You may use this [README template](https://github.com/UtrechtUniversity/rse-project-templates/blob/master/README-template.md)

### Step 5: Change the license file
- Open `LICENSE`, change the copyright holder when required (line 3)
- Or replace the entire license file if another license applies

### Step 6: Add a citation file
- Create a citation file for your repository using [cffinit](https://citation-file-format.github.io/cff-initializer-javascript/#/)

### Step 7: Publising on Pypi (optional/later)
For publishing the package on Pypi you need to create [API tokens](https://docs.github.com/en/actions/automating-builds-and-tests/building-and-testing-python#publishing-to-package-registries).
