# GA–WaOA–LSTM Stock Price Forecasting

A hybrid stock-price forecasting project that combines:

* **LSTM** for time-series prediction
* **Genetic Algorithm (GA)** for global search
* **Walrus Optimization Algorithm (WaOA)** for local optimization

The GA–WaOA algorithm optimizes the LSTM hyperparameters, including the number of units, dropout rate, batch size, and learning rate.

## Dataset

The project uses daily OHLCV stock data downloaded with `yfinance` for:

* VV: `600300.SS`
* LH: `600186.SS`
* SY: `600429.SS`

Eight previous trading days are used to predict the next closing price.

## Features

* Leakage-safe chronological data splitting
* Training-only Min–Max scaling
* Dynamic GA–WaOA optimization
* Early stopping
* Fast, middle, and full experiment modes
* Automatic saving of models, figures, and results
* Evaluation using MAE, MAPE, RMSE, and R²

## Installation

```bash
pip install numpy pandas matplotlib scikit-learn yfinance tqdm tensorflow jupyter
```

## Usage

Open the notebook:

```text
GA_WaOA_LSTM_Stock_Forecasting.ipynb
```

Select the experiment mode:

```python
EXPERIMENT_MODE = "fast"
```

Available modes:

* `fast`: testing and debugging
* `middle`: development experiments
* `full`: final experiment

Run all notebook cells from top to bottom.

## Model Comparisons

The notebook can compare:

* Baseline LSTM
* GA–LSTM
* WaOA–LSTM
* GA–WaOA–LSTM

Enable the required models in the configuration section.

## Outputs

The project automatically saves:

```text
data/
figures/
models/
outputs/
```

Final metrics are saved in:

```text
outputs/results_metrics.csv
```

## Disclaimer

This project is intended for research and educational purposes only and does not provide financial advice.
