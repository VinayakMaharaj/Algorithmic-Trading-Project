# 📈 Algorithmic Trading: ML-Driven Unsupervised Portfolio Strategy

This project implements a full **quantitative trading pipeline** using machine learning, financial factor modeling, and portfolio optimization techniques. It is focused on discovering and backtesting **unsupervised learning-based strategies** using real market data.

> ✅ Built with Python, yFinance, scikit-learn, statsmodels, and PyPortfolioOpt  
> 📊 Visualizes performance vs. S&P 500  
> 🧠 Applies KMeans clustering + factor regression to build smart portfolios  
> 🧮 Optimizes asset allocation using Efficient Frontier  

![Cumulative Returns](./images/cumulative_returns.png)
*Sample visualization: Strategy vs. S&P 500 cumulative return*

---

## 🚀 Project Goals

- Simulate an end-to-end ML-based trading strategy
- Cluster assets by technical & factor exposures
- Allocate capital using modern portfolio theory
- Benchmark strategy vs. passive SP500 index

---

## 🧰 Tools & Libraries Used

- `pandas`, `numpy`, `matplotlib`
- `statsmodels`, `scikit-learn`, `pandas_datareader`
- `yfinance`, `pandas_ta`
- `PyPortfolioOpt` for portfolio optimization

---

## 🧠 Strategy Overview

1. **Data Collection**
   - Load historical price data for all S&P 500 stocks using `yfinance`
   - Pull Fama-French 5-Factor data for macro exposure

2. **Feature Engineering**
   - Monthly aggregation of technical indicators:
     - Garman-Klass volatility
     - RSI, MACD, ATR, Bollinger Bands
     - Dollar volume
   - Rolling factor exposures via linear regression (factor betas)

3. **Unsupervised Learning**
   - Apply **K-Means clustering** each month to segment stocks by risk/return/factor profiles
   - Choose optimal cluster based on characteristics (e.g. low volatility, high Sharpe)

4. **Portfolio Optimization**
   - Use **Efficient Frontier** to select max Sharpe portfolios from clustered assets
   - Leverage `PyPortfolioOpt` for weights and constraints

5. **Evaluation**
   - Compare strategy returns vs. S&P 500
   - Plot cumulative returns, drawdowns, monthly returns

---

## 📊 Results

- Strategy outperformed or matched S&P 500 returns in key timeframes
- Visualizations include:
  - Cumulative return comparison
  - Monthly performance bar charts
  - Cluster distributions and stock selection summaries

---

## 📁 Notebook Sections

- `1_data_preparation.ipynb` – Load and clean data
- `2_feature_engineering.ipynb` – Add technical & factor indicators
- `3_clustering_model.ipynb` – Train KMeans on monthly snapshots
- `4_portfolio_optimization.ipynb` – Efficient frontier + allocation
- `5_evaluation.ipynb` – Return comparison and performance metrics

---

## 🧪 How to Run

> Run this project directly in **Google Colab** or any local Jupyter environment.

1. Clone the repository  
2. Install dependencies: `pip install -r requirements.txt`  
3. Open the `.ipynb` notebook and run all cells

---

## 🧑‍💻 What You’ll Learn

- How to preprocess financial time series for ML
- How to extract and use factor exposures
- How to combine **unsupervised learning** + **portfolio optimization**
- How to build a backtest loop using monthly rolling windows

---

## 🏁 Future Work

- Add **sentiment-based factors** (e.g. Twitter/Finnhub)
- Implement **Reinforcement Learning agent**
- Add **transaction cost modeling**
- Deploy a Gradio dashboard for dynamic simulation

---

## 💡 Inspiration

Inspired by research from:
- “Machine Learning for Asset Managers” by Marcos López de Prado
- Quantopian/QuantConnect community strategies
- Fama-French academic factor models

---

## 🌐 Demo

If you'd like to see a live version or run it in the browser, check out the [Colab Notebook](https://colab.research.google.com/) or use the Gradio app (coming soon).

---

## 📜 License

This project is open-source under the MIT license. Use it, build on it, and make it your own!

