# Python packaging template with Setuptools

This template repository is created by the [UU Research Engineering team](https://utrechtuniversity.github.io/research-engineering/) and is aimed to provide a simple project template for python package development. This template uses [Setuptools](https://setuptools.pypa.io/en/latest/userguide/quickstart.html) as the packaging toolkit, there is another [template](https://github.com/UtrechtUniversity/re-python-package-poetry) that is very similar that uses [Poetry](https://python-poetry.org/).

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

## Next Steps

Now that you have succesfully created a package, there are some further steps to consider.

### Tagging your commits

When your library grows, you might want to give some commits (on main) a more human-readable tag, such as 1.2.0. To do this, do the following:

```bash
git checkout main && git pull
git tag -a "v1.2.0" -m "Version 1.2.0"
git push --tags  # upload the tags to GitHub
```

### Publishing on Pypi 
For publishing the package on Pypi you need to create [API tokens](https://docs.github.com/en/actions/automating-builds-and-tests/building-and-testing-python#publishing-to-package-registries).

If you put this token in GitHub secrets with the name `PYPI_API_TOKEN`, then you can automatically generate a new release on PyPi by creating a release on GitHub. You have to select the tag that was created in the previous step.

Note however that your first release on PyPi has to be done manually and can't be done using this method.
