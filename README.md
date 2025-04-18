# 📈 East African Breweries Ltd Stock Price Prediction Analysis

## 📝 Overview
This project uses an LSTM neural network to predict East African Breweries Ltd's stock closing prices. The analysis includes data preprocessing, exploratory data analysis (EDA), model training, and evaluation. The model achieved **97.51% accuracy** with an RMSE of **0.0248**, demonstrating strong performance in forecasting.

---

## 📚 Table of Contents
1. [📊 Dataset](#dataset)
2. [⚙️ Prerequisites](#prerequisites)
3. [📥 Installation](#installation)
4. [🔍 Methodology](#methodology)
5. [📈 Results](#results)
6. [✅ Conclusion](#conclusion)
7. [📖 References](#references)

---

## 📊 Dataset
- **Source**: Historical stock price data for East African Breweries Ltd (`EastAfricanBreweriesLtdHistoricalPrices.csv`) from the Wall Street Journal (WSL).
- **Features**: Date, Open, High, Low, Close, Volume.
- **Timeframe**: January 2000 to December 2024 (6,134 entries).

---

## ⚙️ Prerequisites
- 🐍 Python 3.8+
- 📦 Libraries:
    - `pandas`, `numpy`, `matplotlib`, `seaborn` (data handling & visualization)
    - `scikit-learn` (preprocessing)
    - `tensorflow` (LSTM model)
    - `math` (evaluation metrics)

---

## 📥 Installation
1. Clone the repository:
     ```bash
     git clone https://github.com/CodeWithEugene/CodeAlpha_STOCK_PREDICTION.git
     ```
2. Install dependencies:
     ```bash
     pip install pandas numpy matplotlib seaborn scikit-learn tensorflow
     ```

---

## 🔍 Methodology

### 1. 🧹 Data Preprocessing
- **Outlier Handling**: IQR-based capping at the 99th percentile to reduce noise.
- **Feature Scaling**: Normalized data using `MinMaxScaler` (range: 0–1).
- **Sequence Creation**: Time-series sequences of 60 days for LSTM input.

### 2. 🧠 Model Architecture
- **Layers**:
    - 2 LSTM layers (50 units each) with dropout (20%) to prevent overfitting.
    - Dense output layer for regression.
- **Training**:
    - Optimizer: Adam.
    - Loss: Mean Squared Error (MSE).
    - Epochs: 10, Batch Size: 32.

### 3. 📏 Evaluation Metrics
- **RMSE**: Root Mean Squared Error.
- **Accuracy**: Derived as `1 - RMSE` (scaled to percentage).

---

## 📈 Results

### 🔑 Key Findings
- **Closing Price Trends**: Visualized historical prices showing volatility and long-term trends.
- **Correlation Matrix**: Strong correlation between Open, High, Low, and Close prices (~99%).
- **Model Performance**: Achieved **97.51% accuracy** on test data with minimal RMSE.

### 📊 Visualizations
- **Price Over Time**: Line plot of closing prices (2000–2024).
- **Volume Trends**: Volume fluctuations aligned with price movements.
- **Outlier Analysis**: Boxplots before/after preprocessing.

---

## ✅ Conclusion
The LSTM model effectively captures temporal patterns in stock data, providing reliable predictions. Future work could incorporate external factors (e.g., news sentiment) or hyperparameter tuning for further optimization.

---

## 📖 References
- 📘 LSTM for Time Series: 
- 📘 Data Preprocessing Techniques: 
- 📘 README Best Practices: 
