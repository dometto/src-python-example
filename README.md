# Python environment managers on Surf Research Cloud

[![Static Badge](https://img.shields.io/badge/Python-black?style=flat-square&logo=python&logoColor=blue&labelColor=gray&color=yellow)](https://www.python.org/)
[![Static Badge](https://img.shields.io/badge/jupyter-blue?style=flat-square&logo=jupyter&logoColor=white&labelColor=gray&color=orange)](https://jupyter.org/)
[![Static Badge](https://img.shields.io/badge/MIT%20License%20-blue?style=flat-square)](https://github.com/UtrechtUniversity/src-jupyter-workshop-template/blob/main/LICENSE)

This repository contains an example project for demonstrating how to work with different Python environment managing tools on SURF Research Cloud. The repository contains multiple files with the same dependencies following different conventions for the different tools used.

## Python tools

The environment managers used are:

- `uv`
- `pyenv`
- `conda`

The main Python libraries used are:

- `geopandas`
- `matplotlib`
- `pandas`
- `shapely`
- `fiona`

## Scenario 1: Python Workbench Desktop 

### Step 1: Clone the repository

1. Open a terminal
2. Clone the repository: `git clone https://github.com/UtrechtUniversity/src-python-example.git`
3. Navigate to the right folder: `cd src-python-example`

### Step 2: Create Environment 

#### Option 1: `uv`
##### Option 1a: From `pyproject.toml` and lockfile `uv.lock`

```
uv sync
source .venv/bin/activate
```

##### Option 1b: From `requirements.txt`

```
uv venv --python 3.10
source .venv/bin/activate
uv pip install -r requirements.txt
```

#### Environment option 2: `pyenv` with requirements.txt

```
pyenv install 3.10
pyenv exec python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

#### Environment option 3: `conda` with environment.yml

```
conda init
conda env create --file=environment.yml
conda activate geo-kernel
```

### Step 3: Run the the Jupyter notebook in VSCodium

- Open VSCodium (Applications > Development > VSCodium)
- Open the folder of the cloned github repo
- Open notebooks/Vectors.ipynb
- Install the required extensions (will be asked to you)
- Select python interpreter (.venv (or geo-kernel in case of conda environment)
- Click: Run all

## Contact

[UU Research Engineering team](https://www.uu.nl/research-engineering)
