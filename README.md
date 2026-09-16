# AALI Stock Price Forecasting with LSTM

An academic deep learning project exploring one-step-ahead stock
price forecasting using a Long Short-Term Memory (LSTM) neural
network trained on historical daily closing-price data of
PT Astra Agro Lestari Tbk (AALI).

## Project Overview

This project was developed as a semester project to explore how
recurrent neural networks, particularly LSTM, can be applied to
time-series forecasting.

The model uses historical AALI closing-price data to learn temporal
patterns and generate one-step-ahead predictions.

> This project is an academic exploration and is not intended to
> provide investment advice or production-ready stock predictions.

## Objective

The main objective is to evaluate whether an LSTM-based neural
network can learn patterns from historical AALI closing-price data
and predict the subsequent closing price.

## Dataset

The dataset contains historical daily stock-price data for
PT Astra Agro Lestari Tbk (AALI).

### Target Variable

- `Close` — daily closing price

The dataset is provided in the `data/` directory.

## Methodology

The project follows these main steps:

1. Load and inspect the historical stock-price dataset.
2. Explore historical closing-price movements.
3. Normalize the closing-price data using MinMaxScaler.
4. Split the data into training and testing sets.
5. Transform the data into sequential input format.
6. Build a stacked LSTM neural network.
7. Train the model using the Adam optimizer and Huber loss.
8. Monitor Mean Absolute Error (MAE) during training.
9. Generate one-step-ahead closing-price predictions.
10. Compare actual and predicted closing prices.

## Model Architecture

The model consists of:

- LSTM layer — 100 units
- LSTM layer — 50 units
- Dense layer — 25 units with ReLU activation
- Dense output layer — 1 unit

## Evaluation

The primary evaluation metric used in the original implementation
is Mean Absolute Error (MAE).

The notebook also provides visual comparisons between actual and
predicted closing prices.

## Results

The final results and model evaluation are presented in the
Jupyter Notebook.

The project demonstrates the application of an LSTM architecture
for one-step-ahead forecasting of historical AALI closing prices.

## Limitations

Several methodological limitations should be considered:

- The original model uses a very short look-back window.
- Data normalization was performed before the train-test split,
  which may introduce data leakage.
- The test set was also used as validation data during training.
- No naive baseline model was included for comparison.
- Evaluation was primarily based on MAE.

These limitations make the project more suitable as an academic
proof of concept rather than a production forecasting system.

## Tech Stack

- Python
- Pandas
- NumPy
- TensorFlow / Keras
- Scikit-learn
- Matplotlib
- Seaborn
- Jupyter Notebook / Google Colab

## Repository Structure

```text
├── README.md
├── AALI_Stock_Price_Forecasting_LSTM.ipynb
├── requirements.txt
└── data/
    └── AALI_daily.csv