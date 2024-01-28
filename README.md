# Temporal Convolution Networks For Energy Demand Forecast: Malta Case Study

Code for the experiments to predict the energy demands in a grid, with datasets from Malta for this usecase.

# Install Common Environment

We created a *python 3.10* env in conda:
```bash
conda env create -f environment.yml
```
but python venv is also possible:
```bash
venv create aml --python=python3.10
venv activate aml
```
Dependencies available in:  **requirements.txt**:
`yes | pip install -r requirements.txt`

## Tensorflow Conda Installation

If you want to install your Tensorflow, install it from conda like this:
```bash
conda config --add channels conda-forge
conda create -n tf tensorflow
conda activate tf
```
or create it with our environment.yml:
```bash
conda env create -n tf -f environment.yml
conda activate tf
```

## Datasets

All CVSs should are available in the folder ['./raw_data'](./raw_data)

## ENV configurations

A default `.env` was provided.
Use your own and add it to `.gitignore`.


## Reference
This is a tensorflow variation of the architecture presented in the paper [Deep Learning for Time Series Forecasting: The Electric Load Case](https://arxiv.org/abs/1907.09207) paper.
Mind that the code has been changed a bit, thus you may notice some differences with the models described in the paper:
```
@article{gasparin2019deep,
  title={Deep Learning for Time Series Forecasting: The Electric Load Case},
  author={Gasparin, Alberto and Lukovic, Slobodan and Alippi, Cesare},
  journal={arXiv preprint arXiv:1907.09207},
  year={2019}
}
```