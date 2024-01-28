# Machine Learning Approaches to Ethical Analysis of Statistics (ICS5110)

Applied ML Assignment collaboration guidelines. Notebook is here: [aml_ICS5110.ipynb](./aml_ICS5110.ipynb).

## Project Structure

- All papers, assignment latex, images, etc. should be stored in the ./misc directory.
- Models should go to ./models, their training meta file to ./logs
- Data should go to ./data or if unprocessed to ./raw_data

## Install Common Environment

Create *python 3.10* env in conda:

```bash
conda env create -f environment.yml
```
or python venv:

```bash
venv create aml --python=python3.10
venv activate aml
```

Install dependencies from **requirements.txt**:
`yes | pip install -r requirements.txt`

## Tensorflow Conda Installation

For our TCN, you can create the conda environment directly through the YML provided: `environment.yml`

If you want to install your Tensorflow, install it from conda like this:

```bash
conda config --add channels conda-forge
conda create -n tf tensorflow
conda activate tf
```

## Commiting the Environment

Use pipreqs to help commit dependencies:

- `pip install pipreqs`
- `pip install nbconvert`

When **commiting**, update the requirements from your base folder:

```bash
jupyter nbconvert --to script *.ipynb 
pipreqs . --encoding=utf8  --force
```

**NB**: the above will generate a file **.py*, this is only needed for pipreqs to capture dependecies. Do not commit (all python files go to the .ignore)

for conda envs, use this:  `conda env export > environment.yml`

## Datasets

Commit datasets as CSV if <10mb, else use LSF.

All CVSs should go to the folder ['./raw_data'](./raw_data)

# Exporting Notebooks

Use: `jupyter nbconvert --to pdf *.ipynb`


## ENV configurations

A default `.env` was provided.
Use your own and add it to `.gitignore`.

API connections, environment variables, and other secrets need to go in your .env.
**Do not commit** your .env!