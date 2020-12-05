# fake-news-ptBR

{TODO: Adicioanar Descrição do Projeto}

## Project Organization

The project's structure is based on the [Cookiecutter Data Science Project Template](https://drivendata.github.io/cookiecutter-data-science/) by Driven Data. We
recommend reading the documentation for a deep understanding on how it works and
the benefits of this approach. For this project the organization occurs as folows:

    ├── LICENSE            <- Project's License of Use
    ├── README.md          <- This document
    ├── data
    │   ├── external       <- Data from third party sources.
    │   ├── interim        <- Intermediate data that has been transformed.
    │   ├── processed      <- The final, canonical data sets for study
    │   └── raw            <- The original, immutable data dump.
    │
    ├── models             <- Trained and serialized models, model predictions, or model summaries
    │
    ├── notebooks          <- The main code of this project on Jupyter notebooks
    │
    ├── references         <- Data dictionaries, manuals, and all other explanatory materials.
    │
    ├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
    │   └── figures        <- Generated graphics and figures to be used in reporting
    │
    ├── poetry.lock        <- Poetry file that configures the virtual environment
    ├── pyproject.toml     <- Build System file configuration (PEP 518)
    └── requirements.txt   <- The requirements file for reproducing the analysis environment

## Installing dependencies

### Recommendation: Managing Python Versions
To avoid problems with different python versions we recommend the use of the
[Pyenv](https://github.com/pyenv/pyenv) tool. This tool helps an easy management
of multiple python versions on the computer. For installation see
[Pyenv Installation](https://github.com/pyenv/pyenv#installation).

This projects uses python 3.8.5. If you are using pyenv, the installation of this
version can be done via:

```shell
pyenv install 3.8.5
```

To make this version the default for this project you can use the command below
(make sure you are on this folder):

```shell
pyenv local 3.8.5
```

### Dependency Management

For dependency management the tool uses is the [Poetry Project](https://python-poetry.org/). For installation see [Poetry Installation](https://python-poetry.org/docs/#installation). After installed, the packages can be used by using the command:

```shell
poetry install
```

For the project to work you still need to activate the virtual environment, this
can be easily done with the command:

```shell
poetry shell
```

For other commands, see [Poetry Commands](https://python-poetry.org/docs/cli/).
If you already uses **another package management tools** we also provide a
*requirements.txt* that can be used on these tools.

## Setup Data

The data used on this project is available at [Fake.br-Corpus Github Page](https://github.com/roneysco/Fake.br-Corpus) on this [commit](https://github.com/roneysco/Fake.br-Corpus/tree/780f5516c4ae070761632d98ac3368f3ded09d35). So, make sure that
you are downloading the correct version of data.

To start using the code, download the data from the repository and place only
the content of the *full_texts* folder into the raw data folder. This is:

    ├── data
        ├── ...
        └── raw
            ├── fake-meta-information
                └── ...
            ├── fake
                └── ...
            ├── true-meta-information
                └── ...
            └── true
                └── ...
