# 📈 Stock Price Trend Prediction with LSTM  
### 🚀 Elevate Labs AI/ML Internship – Final Project  
**Stock Ticker: MSFT (Microsoft Corporation)**

---

## 🎯 Objective

To develop an LSTM-based deep learning model to predict **Microsoft (MSFT)** stock price trends using historical data. The project also integrates **technical indicators** like Moving Average (MA) and Relative Strength Index (RSI) to enhance prediction context and interpretability.

---

## 🛠 Tools & Libraries

| Tool            | Purpose                                   |
|-----------------|-------------------------------------------|
| Python          | Programming language                      |
| Pandas, NumPy   | Data manipulation and analysis            |
| yfinance        | Fetching historical stock data            |
| Matplotlib      | Data visualization                        |
| Scikit-learn    | Preprocessing (`MinMaxScaler`)            |
| Keras (TensorFlow) | LSTM model building and training     |
| ta (Technical Analysis) | Calculating MA & RSI           |

---

## 📂 Dataset

- **Source**: Yahoo Finance (via `yfinance`)
- **Ticker**: `MSFT` (Microsoft)
- **Period**: January 1, 2015 – December 31, 2023
- **Target Feature**: `Close` price
- **Other Columns**: `Open`, `High`, `Low`, `Volume`, `Dividends`, `Stock Splits`

---

## 🔁 Steps Followed

### 1. 📥 Data Fetching
Downloaded historical MSFT data using `yfinance` API.

### 2. 📊 Technical Indicators
- **MA20**: 20-day moving average
- **RSI**: 14-period Relative Strength Index using `ta.momentum.RSIIndicator`

### 3. 🧹 Data Preprocessing
- Dropped rows with missing values due to MA/RSI windows.
- Extracted `Close` prices and normalized them between 0 and 1 using `MinMaxScaler`.

### 4. 🔗 Sequence Creation
- Created 60-day sequences to predict the next day's closing price.

### 5. 🧪 Train-Test Split
- 80% training data and 20% testing data.

### 6. 🧠 Model Architecture
- Stacked LSTM layers with dropout.
- Compiled with `adam` optimizer and `mean_squared_error` loss.

### 7. 📚 Model Training
- Trained for 20 epochs with batch size of 64.

### 8. 🔮 Prediction & Evaluation
- Predicted prices on test data.
- Inverse-scaled results to original price scale.
- Plotted:
  - Training predictions
  - Overall predictions
  - Closing prices with MA20 and RSI

---

## 📊 Output Visualizations

Saved under `plots/`:

- `MSFT_training_prediction.png` – Model fit on training data  
- `MSFT_overall_prediction.png` – Prediction vs. actual on full dataset  
- `MSFT_indicators_plot.png` – Close price with MA20 and RSI overlay

---

## 🧠 Key Learnings

- Gained experience in **time-series forecasting** with LSTM.
- Learned to use **technical indicators** to enhance stock trend analysis.
- Built a complete end-to-end AI/ML pipeline from **data fetching to visualization**.

---

## ⚠️ Disclaimer

This project is for **educational purposes only**. It should **not be used** for real-world trading or financial decisions.

---

## 🙌 Acknowledgment

Grateful to **Elevate Labs** for guiding and mentoring throughout this AI/ML internship. This project showcases real-world application of machine learning in financial analytics.

