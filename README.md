# Understanding Fake News in Portuguese

This repository contains all the data and code used to understand and model the [Fake.br-Corpus](https://github.com/roneysco/Fake.br-Corpus).

## Preparing the Environment
This section explains how to use/reproduce this project. Note that this tutorial is made to work on a linux machine.

### 1. Installing Python

#### PyEnv
This projects used Python 3.8.5. For management of multiple python versions we recommend the installation of [Pyenv](https://github.com/pyenv/pyenv). For installation of the tool visit [Pyenv Installation](https://github.com/pyenv/pyenv#installation). After the installation you are ready to install the python version by using the command:

```shell
pyenv install 3.8.7
```
To make this version the default for this project you can use the command below (make sure you are on this folder): 

```shell
pyenv local 3.8.7
```

#### Without PyEnv
If you don't want to use pyenv, make sure you are using the correct version of python. You can see instruction on how to install python on [Python Downloads](https://www.python.org/downloads/).

### 2. Python Libraries and Virtual Environments (Dependency Manager)
#### Poetry
For dependency management we use the [Poetry Project](https://python-poetry.org/). For installation see [Poetry Installation](https://python-poetry.org/docs/#installation). After the installation, all the packages used by this project can be installed via:
```shell
poetry install
```
To use the packages, you also need to activate the environment by using the command:
```shell
poetry shell
```
For other commands, see [Poetry Commands](https://python-poetry.org/docs/cli/).

#### Other Dependency Management or No Virtual Environments
If you don't want to use Poetry or any virtual environments, we provide a "requirements.txt" file. To install this on your version of python:

```shell
python -m pip install -r requirements.txt
```
### 3. Installing R
This project uses R for the modeling phase. Make sure you install version 4.1.
For package management we use [packrat](https://rstudio.github.io/packrat/). To
setup packrat open R using the command ```R``` on shell. After that

```R
install.packages("packrat")
```

### 4. Setup Jupyter Notebook to use R
To use Jupyter with R use the command below to make the kernel available to
all Jupyter. On R console, execute:

```R
IRkernel::installspec(user = FALSE)
```

### 5. Install NPM and NodeJS to use jupyter Widgets
You also need to install NPM and NodeJS to be able to use IPywidgets in this
project. You can do this by running:

```shell
apt install npm nodejs
jupyter labextension install @jupyter-widgets/jupyterlab-manager
```
**NOTE:** You can see more information about how to setup on
[Ipywidgets: Installation](https://ipywidgets.readthedocs.io/en/latest/user_install.html). 


## Data
All the data used on this project and their transformations can be found in the data folder of this repository. The raw data was acquired on the [Fake.br-Corpus](https://github.com/roneysco/Fake.br-Corpus) repository on this [commit](https://github.com/roneysco/Fake.br-Corpus/tree/780f5516c4ae070761632d98ac3368f3ded09d35).

## Project Structure
The project's structure is based on the [Cookiecutter Data Science Project Template](https://drivendata.github.io/cookiecutter-data-science/) by Driven Data. We recommend reading the documentation for a deep understanding on how it works and the benefits of this approach. For this project the organization occurs as folows:

    ├── LICENSE            <- Project's License of Use
    ├── README.md          <- This document
    ├── data
    │   ├── external       <- Data from third party sources.
    │   ├── interim        <- Intermediate data that has been transformed.
    │   ├── processed      <- The final, canonical data sets for study
    │   └── raw            <- The original, immutable data dump.
    ├── notebooks          <- The main code of this project on Jupyter notebooks
    ├── packrat            <- R package management files
    │   ├── init.R
    │   ├── packrat.lock
    │   └── packrat.opts
    ├── references         <- Data dictionaries, manuals, and all other explanatory materials.
    ├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
    │   └── figures        <- Generated graphics and figures to be used in reporting
    ├── poetry.lock        <- Poetry file that configures the virtual environment
    ├── pyproject.toml     <- Build System file configuration (PEP 518)
    └── requirements.txt   <- The requirements file for reproducing the analysis environment
