# Contributing

Welcome to axem's contribution guide. We would like to work together with anyone and everyone in a 
fun, enjoyable, and educational  way. To achieve this please follow our 
[CoC](https://github.com/axem-solutions/.github/blob/main/CODE_OF_CONDUCT.md).

All contributions, including new features, bug fixes, new docs, graphics, and more are welcome. 
Please create new issues for bugs, feature ideas, or any improvements.

Reach out to us at 
- [Discussions](https://github.com/axem-solutions/dem/discussions)
- [Discord](https://discord.com/invite/Nv6hSzXruK)
- Send a DM on GitHub or an email to info@axemsoutions.io

Before contributing don't forget to read the DEM's [documentation](https://axemsolutions.io/dem_doc/) 
or try the [tutorial](https://www.axemsolutions.io/tutorial/) for hand-on experience.

## Creating a new issue

1. Select 'New issue'
2. Select issue type
3. Write a small description as the Title
4. Fill the issue template
5. Set extra labels if needed
6. Set the project to *DEM Open* and status to 🆕 New
7. Submit the new issue

## Working on an issue

1. Select an issue which has the status 🔖 Ready to implement under the issue's project settings
2. Discuss the selected issue with the maintainers -> you can reach out at the
[Discussions](https://github.com/axem-solutions/dem/discussions) or [Discord](https://discord.com/invite/Nv6hSzXruK)
3. Set the selected issue's status to 🏗️ In progress when you start to work on it
4. Fork the DEM, if you haven't done it already
5. Create a new feature branch for your modifications (you can name it as you wish, but our
best practice is to name it after the issue ID)
6. Create the implementation
7. Open a PR from your fork to the upstream main and fill the PR template
8. Set the *persea* group as reviewer, then set the issue's status to 👀 In review
9. Fix the findings if there is any
10. The reviewer who approved the PR can set the status to ✅ Done
11. The branch can be merged to the upstream main

## Working with the DEM source

> The following steps are mandatory to be able to work with the DEM source.

We use [poetry](https://python-poetry.org/) to manage dependencies and create a 
virtual environment for DEM. Install it with: 

   curl -sSL https://install.python-poetry.org | python3 - 

You should enter the preconfigured virtual environment to ensure that you use 
the correct version of the required modules.

First, install the environment with the required dependencies:

    poetry install

Enter the virtual environment:

    poetry shell

The recommended way to test your modifications is to use the poetry shell.

As an alternative, you can use DEM as a Python module. To do this, you must add 
the `-m` flag to your command.

For example:

    python -m dem list --local --env

## Running Unit Tests

Run unit tests:

    pytest tests

Run unit tests with coverage information as HTML:

    pytest --cov-report=html --cov=dem tests/

If you'd like the coverage results right in your terminal:

    pytest --cov-report term-missing --cov=dem tests/
