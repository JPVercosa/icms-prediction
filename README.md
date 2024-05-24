# ICMS Prediction for Rio de Janeiro

This repository contains the code and data used in the article "Estudo de Modelos para a Previsão de Arrecadação do ICMS do Rio de Janeiro" by João Pedro Verçosa. The study explores various machine learning models to forecast the ICMS revenue in Rio de Janeiro, using data from 2004 to 2022.

## Table of Contents

1. [Introduction](#introduction)
2. [Data](#data)
3. [Models](#models)
4. [Usage](#usage)
5. [Results](#results)

## Introduction

The purpose of this study is to analyze and predict the ICMS revenue in Rio de Janeiro using advanced machine learning techniques. The models used include Random Forest, XGBoost, and Long Short-Term Memory (LSTM) neural networks. The study aims to provide more accurate forecasting to support government planning and decision-making.

## Data

The dataset includes time series data from various economic and social indicators, that were compared with the ICMS time series using DTW ([Dynamic Time Warping notebook](/notebooks/dtw.ipynb)) technique. They were collected from open data sources such as the Portal de Dados Abertos[^1], SGS-Sistema Gerenciador de Séries Temporais[^2], and the Empresa de Pesquisa Energética[^3]. The data used in this study is available in the `data` directory of this repository.

## Models

The models explored in this study are:

- **Random Forest**
- **XGBoost**
- **LSTM Neural Networks**

Each model is trained and evaluated using a set of parameters optimized through Grid Search. Details on the parameter values and optimization process are provided in the article and the accompanying Jupyter notebooks in this repository.

## Usage

To run the code, you need to have Python installed with the required libraries. You can install the dependencies using the provided `requirements.txt` file.

```bash
pip install -r requirements.txt
```

### Running the Models

Each model has its own Jupyter notebook in the `notebooks` directory:

- [`random_forest.ipynb`](notebooks/random_forest.ipynb)
- [`xgboost.ipynb`](notebooks/xgboost.ipynb)
- [`LSTM.ipynb`](notebooks/lstm.ipynb)

You can open and run these notebooks to reproduce the results of the study. The notebooks include all the steps from data preprocessing, model training, and evaluation.

### Data Preprocessing

The data preprocessing steps are included in the `preprocessing.ipynb` script. This script normalizes the data and prepares it for model training. Run the [`preprocessing.ipynb`](notebooks/preprocessing.ipynb) to get everything ready.

## Results

The study found that the Random Forest and XGBoost models performed better than the LSTM model in terms of predictive accuracy. The best performance was achieved using a multivariate approach with ICMS and total oil production series, yielding a Mean Absolute Percentage Error (MAPE) of 10.01% over a 12-month forecast horizon.

For more detailed information, please refer to the full article (in Portuguese) that can be found here: [Estudo de Modelos para aPrevisão de Arracadação do ICMS do Rio de Janeiro](https://www.dropbox.com/scl/fi/v0057zg7am3dao9g06q8q/Estudo_de_Modelos_para_a_Previs-o_de_Arrecada-o_do_ICMS_do_Rio_de_Janeiro-Jo-o-Pedro-Ver-osa.pdf?rlkey=xg5bjvlxf9e14jix8ji9zreaq&dl=0).

[^1]: [Portal de Dados Abertos](https://dados.gov.br/)
[^2]: [SGS-Sistema Gerenciador de Séries Temporais](https://www3.bcb.gov.br/sgspub)
[^3]: [Empresa de Pesquisa Energética](https://www.epe.gov.br/pt/publicacoes-dados-abertos/publicacoes)
[^4]: João Pedro Knauer de Queiroz Verçosa, [GitHub Repository](https://github.com/JPVercosa/icms-prediction)

