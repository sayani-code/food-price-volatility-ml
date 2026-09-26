# Food Price Volatility & Market Risk Prediction Using Machine Learning

A machine learning project for classifying food-market price volatility risk using historical mandi market price data.

## Project Overview

Food prices can fluctuate significantly across commodities and markets. Instead of predicting the exact future price, this project investigates whether machine learning can identify whether a food commodity in a particular market is likely to experience higher price volatility in the near future.

The primary ML task is to classify volatility risk into:

* Low Volatility
* Medium Volatility
* High Volatility

## Problem Statement

Can machine learning predict whether a food commodity in a particular market is likely to experience high price volatility in the near future?

This project treats the problem as a classification task rather than direct price prediction.

## Data Source

The project will use historical food-market price data from the Government of India's Open Government Data platform.

Dataset:

**Current Daily Price of Various Commodities from Various Markets (Mandi)**

Source: data.gov.in

The dataset contains market-level information such as:

* State
* District
* Market
* Commodity
* Variety
* Arrival Date
* Minimum Price
* Maximum Price
* Modal Price

The Modal Price will initially be considered as the primary price variable. This decision will be reviewed after inspecting the actual dataset.

## Initial Commodity Scope

The initial commodities under consideration are:

* Tomato
* Onion
* Potato

The final geographic and market scope will be determined after inspecting the actual dataset.

## Machine Learning Workflow

The project will follow an end-to-end machine learning workflow:

1. Problem Definition
2. Dataset Collection
3. Data Understanding
4. Data Cleaning
5. Exploratory Data Analysis
6. Volatility Target Definition
7. Feature Engineering
8. Time-Aware Train/Validation/Test Split
9. Baseline Model
10. Model Training
11. Hyperparameter Tuning
12. Model Evaluation
13. Error Analysis
14. Feature Importance / Explainability
15. Prediction Application
16. GitHub Documentation
17. Portfolio Presentation

## Time-Aware Machine Learning

Because the dataset is time-dependent, chronological validation will be used instead of an unjustified random train/test split.

Feature engineering will also be designed to prevent future information from leaking into the training data.

## Volatility Definition

The Low, Medium, and High volatility categories will not be defined using an arbitrary threshold before inspecting the data.

The project will first investigate:

* Daily price changes / returns
* Rolling volatility
* Volatility distributions
* Class balance

The final target definition will be based on the observed data and will be documented clearly.

## Planned Features

Potential features include:

* Lagged prices
* Price changes
* Rolling statistics
* Momentum/change features
* Calendar features
* Market information
* Commodity information

Only features that are appropriate after inspecting the actual dataset will be retained.

## Planned Models

The project will progressively evaluate:

* Baseline
* Logistic Regression
* Random Forest
* Gradient Boosting / XGBoost

Models will only be retained when they provide meaningful technical or practical value.

## Evaluation

Model performance will be evaluated using appropriate classification metrics, including:

* Precision
* Recall
* F1-score
* Confusion Matrix
* ROC-AUC where appropriate
* PR-AUC where useful

Particular attention will be given to the High Volatility class.

## Explainability

The project will investigate model feature importance to understand which historical price characteristics contribute to volatility-risk predictions.

SHAP may be considered later if it provides meaningful additional interpretability.

## Final Application

A Streamlit-based application is planned as the final user interface.

The application will use the actual trained model to generate volatility-risk predictions.

No prediction values will be fabricated for demonstration purposes.

## Project Structure

```text
food-price-volatility-ml/
│
├── data/
│   ├── raw/
│   └── processed/
│
├── notebooks/
│   ├── 01_data_understanding.ipynb
│   ├── 02_eda.ipynb
│   ├── 03_target_and_features.ipynb
│   └── 04_model_training.ipynb
│
├── src/
│   ├── __init__.py
│   ├── preprocessing.py
│   ├── features.py
│   ├── train.py
│   └── predict.py
│
├── models/
│
├── app/
│   └── app.py
│
├── reports/
│   └── figures/
│
├── requirements.txt
├── README.md
├── .gitignore
└── LICENSE
```

## Project Status

🚧 **Phase 0 — Project Setup**

The project is currently in the initial setup stage. Dataset inspection and model training have not started yet.

## Disclaimer

This project is intended as a machine learning portfolio and educational project. Its predictions should not be interpreted as guaranteed forecasts of future food prices or market conditions.
