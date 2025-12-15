# 📈 Stock Price Predictor
![Python Version](https://img.shields.io/badge/python-3.8%2B-blue)

This notebook is a short, practical project that walks through fetching S&P 500 OHLCV data, engineering time-series features, and building a simple yet informative Random Forest baseline to predict whether the index will close higher the next day.

Why this is fun and useful:
- Learn real-world time-series data handling (no leakage, rolling-window validation).
- See how a few compact features (multi-horizon ratios & trend counts) can power a baseline model.
- Reproduce the pipeline locally or on Binder/Colab for quick experimentation.

## 🔍 What you'll find
- **Data fetch & inspect:** download `^GSPC` with `yfinance` and plot Close price trends.
- **Target:** `Tomorrow` and binary `Target` (next-day up/down).
- **Features:** `Close_Ratio_{h}` and `Trend_{h}` for horizons [2, 5, 60, 250, 1000].
- **Modeling:** Random Forest baseline, probability thresholding, and rolling-window `backtest()`.

## 🚀 Set Up
1. Clone and enter the directory:

```bash
git clone <your-repo-url>
cd stock_predictor_nb
```

2. Recommended: create a virtual environment and install the minimal dependencies:

```bash
python -m venv .venv
source .venv/bin/activate  # macOS / Linux
pip install -r ../requirements.txt
```

3. Launch Jupyter and run the notebook:

```bash
jupyter notebook
# open stock_predictor.ipynb
```

Tip: Use `pip freeze > requirements.txt` to pin versions when you want exact reproducibility.

## ✅ Quick outcomes 
- How to avoid look-ahead bias when engineering features and creating targets.
- How to use rolling-window backtests for time-aware model evaluation.
- How to convert model probabilities into actionable, thresholded predictions.

## ✍️ Project goals & contributions
- **Goal:** Build a small, reproducible pipeline that demonstrates core concepts in financial time-series modeling and model evaluation.
- **Contributions:** Notebook authoring, `yfinance` data ingestion, multi-horizon feature engineering, baseline model, and backtest utilities.

## 💡 Next steps / Ideas to try
- Add more features (technical indicators, volatility, macro series).
- Replace Random Forest with LightGBM / XGBoost and run grid search.
- Implement a simulated trading loop to estimate economic performance (returns, transaction costs, risk metrics).

## 🙏 Credits
Inspired by Dataquest's YouTube tutorials on practical data projects — thanks for the clear guidance!


