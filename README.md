# 🏀 Predicting 3-Point Records in the NBA: Will Anyone Surpass Stephen Curry?

This project explores historical NBA player data to analyze trends in 3-point shooting, and evaluates whether it is statistically feasible for a player to surpass **Stephen Curry’s single-season record of 402 three-pointers made**. It also builds predictive models to estimate 3-point makes based on player performance variables, emphasizing game style changes and shot selection metrics.

---

## 🎯 Research Questions

- What factors contribute to high-volume 3-point shooters?
- Can a player realistically break Curry’s record of 402 3PM in a season?
- Can we predict a player’s 3-point makes using prior performance data?

---

## 📦 Data Description

- **Sources**:  
  - Kaggle datasets originally derived from [Basketball Reference](https://www.basketball-reference.com)
  - Two datasets merged: player stats and shot breakdowns (1997–2023)

- **Key Variables**:
  - `3PM`, `3PA`, `3P%`
  - `Corner 3P%`, `Percent Assisted`, `Minutes Played`
  - Game-by-game and season-by-season splits

- **Data Wrangling**:
  - Cleaned seasons and merged datasets by `Player` and `Season`
  - Added per-game metrics (3PM/game, 3PA/game)
  - Filtered out irrelevant years and filled missing values

---

## 📊 Methodology

### 🔍 Exploratory Data Analysis
- Trend plots: increase in 3PA and 3PM over time
- Highlighted top players: Harden, Klay, Lillard, Hield, Curry
- Visualized corner 3-point trends and assisted shot rates

### 📈 Linear Regression Models
- Target variable: Total 3-point makes per season
- Predictor variables:
  - `3P%`
  - `Corner 3P%`
  - `Percent of 3P Assisted`
  - `3PA`

> **R² ≈ 0.98** — strong linear relationship, with 3PA as most influential predictor

### ⏱️ Time Series Forecasting
- Built a time-series model on Curry’s historical stats
- Forecasted future 3PM values using the `forecast()` package in R
- Evaluated prediction accuracy with RMSE

---

## 📉 Key Findings

- Curry’s record of **402 3PM in a season** requires:
  - ~900 attempts at 45% 3P%
  - ~11 3P attempts/game, 82 games played

- **3PA is the strongest predictor** of 3PM, followed by corner 3P% and assist rate

- Linear regression model yielded strong fit, but forecasting failed to predict irregular season impacts (e.g., COVID-shortened 2020)

- **RMSE Results**:
  - 2020 Prediction Error: 257.78 (due to COVID season)
  - 2021 Prediction Error: 67.44

---

## 📁 Repository Contents

- `3Point Shooting Project.pdf` – Full write-up
- `code/` – Data cleaning, regression, and forecasting scripts in R
- `figures/` – Visualizations for 3PM trends, model outputs, and predictions
- `README.md` – This summary file

---

## 📚 Tools Used

- R (dplyr, ggplot2, forecast, caret)
- Kaggle Datasets
- Basketball Reference-derived stats

---

## 💡 Reflection & Future Work

- Include up-to-date data through 2023 or 2024
- Improve forecasting model with non-linear or machine learning techniques
- Add context-based predictors (e.g., usage rate, team pace, roster changes)
- Expand to include player tracking stats for deeper analysis

---

## 👤 Author

**Brett Loy**  
 
