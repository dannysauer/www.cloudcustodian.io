# Cloud Custodian Website docs

This repo generates the website of cloud custodian at https://cloudcustodian.io

It uses mkdocs to build a static site.

When creating pull requests, staging previews are created at
http://docs-stage.cloudcustodian.io.s3-website-us-east-1.amazonaws.com/docs/{{pull_request_number}}/


## Getting Started

* Make sure to have [Python 3.8+ installed](https://www.python.org/downloads/)
* Make sure to have [Poetry 1.2+ installed](https://python-poetry.org/docs/)

Clone this repository to your local machine. Navigate to the directory and run the following command to install dependencies:


```
poetry install
```

Run the docs locally

```
poetry run mkdocs serve
```

Navigate to http://localhost:8000 to view the rendered site!

## Adding new plugins / dependencies

Update the pyproject.toml file using the poetry add command:

```
poetry add <package>
```

Often, plugins will instruct using `pip install` or updating a `requirements.txt`. For example, if a plugin says to use `pip install my_plugin` run `poetry add my_plugin` instead.
Once installed, add the plugin and any plugin configuration to `mkdocs.yml`. Finally, make sure to commit both the pyproject.toml and poetry.lock files.
