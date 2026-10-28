# Machine Learning for Financial Market Data

A machine learning project exploring financial time-series data using technical indicators, feature engineering and predictive models.

The project investigates how traditional machine learning algorithms and neural networks can be applied to Ethereum/GBP market data, with a focus on data preprocessing, model comparison and evaluation.

## Overview

Financial market data is noisy, non-stationary and time-dependent. This project explores different modelling approaches for analysing market data and evaluating their predictive performance.

The work includes:

- Exploratory analysis of Ethereum/GBP bid and ask price data.
- Feature engineering using technical indicators.
- Data preprocessing and preparation for supervised learning.
- Comparison of traditional machine learning algorithms and neural networks.
- Model evaluation using appropriate performance metrics.

**Project status:** University project / experimental research.

## Dataset

The project uses historical Ethereum/GBP market data containing minute-level bid and ask prices.

The dataset is used to investigate the relationship between market features and the selected prediction target.

Dataset details:

- **Asset:** Ethereum / GBP (ETH/GBP)
- **Frequency:** Minute-level observations
- **Price data:** Bid and ask prices
- **Features:** Price-derived technical indicators and engineered features
- **Prediction target:** Predict the highest and lowest prices during the next 5 minutes.
- **Data source:** Dukascopy Bank

## Feature Engineering

The project explores technical indicators and derived market features, including:

- Relative Strength Index (RSI)
- Moving Average Convergence Divergence (MACD)
- Bollinger Bands
- Moving averages
- Alligator-style indicator features

These features provide different representations of recent price movements, momentum and volatility.

Feature calculations should use only information available at the relevant prediction time. Any rolling calculations, scaling or feature selection must be designed to avoid leaking future information into the training data.

## Models

The experiments explore a range of machine learning approaches.

| Model family | Models |
|---|---|
| Regression | K-Nearest Neighbours, Random Forest, Stochastic Gradient Descent |
| Gradient boosting | XGBoost |
| Neural networks | Multilayer Perceptron (MLP), Convolutional Neural Network (CNN), Long Short-Term Memory (LSTM) |

The models are intended for comparison under a consistent evaluation procedure. The exact models, hyperparameters and results should be documented alongside the corresponding experiments.

## Methodology

The general workflow is:

1. Load and inspect the historical market data.
2. Clean and preprocess the observations.
3. Engineer features from price data and technical indicators.
4. Define the prediction target and forecast horizon.
5. Split observations chronologically into training, validation and test sets.
6. Train models and tune hyperparameters using training and validation data.
7. Evaluate the final models on held-out test data.
8. Compare results and discuss limitations.

For time-series data, a chronological split is preferable to a random split because randomly mixing observations can introduce leakage and produce overly optimistic results.

Any normalisation or feature selection should be fitted using training data only.

## Evaluation

Model performance should be assessed using metrics appropriate to the chosen prediction target.

For a continuous price or return prediction task, possible metrics include:

- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- Coefficient of determination (R²), where appropriate

If the task predicts price direction or another class, classification metrics may be more appropriate.

## Installation

Clone the repository:

```bash
git clone https://github.com/Zagyarakushi/Machine-Learning-for-Financial-Market-Data/
cd machine-learning-for-financial-market-data
```

## Usage

Start with the notebooks to explore the data, reproduce feature engineering and inspect model evaluation.

## Limitations

- Financial time series are noisy and their statistical properties can change over time.
- Strong historical test performance does not guarantee performance on future data.
- Results can be affected by data quality, feature selection, hyperparameter tuning and leakage.
- Price-prediction accuracy does not by itself establish trading profitability.
- Transaction costs, bid-ask spreads, slippage and execution constraints would need to be considered before evaluating a trading strategy.

## Future Improvements

Potential extensions include:

- Walk-forward validation and evaluation across different market conditions.
- Comparison against simple statistical and persistence baselines.
- More systematic hyperparameter tuning.
- Analysis of feature importance and model behaviour.
- Evaluation of robustness across different test periods.
- Transaction-cost-aware backtesting, if a trading strategy is explicitly implemented.

## Technologies

- Python
- pandas and NumPy
- scikit-learn
- TensorFlow / Keras
- XGBoost
- Jupyter Notebook
- Matplotlib / Seaborn

## Disclaimer

This repository is an educational machine learning project. It is not financial advice and does not establish that any model can reliably predict market prices or generate profitable trading returns.

## Author

**Charles Buckley**

- GitHub: [zagyarakushi](https://github.com/zagyarakushi)
- GitLab: [zagyarakushi](https://gitlab.com/zagyarakushi)