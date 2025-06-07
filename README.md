 # 📈 Stock Price Prediction Using Deep Learning (RNN, LSTM, GRU, Conv1D)

This project aims to forecast the **next-day closing price of Amazon stock (AMZN)** using historical time series data from Yahoo Finance. The analysis compares the performance of multiple deep learning models — **RNN, LSTM, GRU, and Conv1D** — in terms of their accuracy and ability to generalize.

---

## 🗂️ Dataset Description

- **Source**: Yahoo Finance
- **Ticker**: AMZN
- **Date Range**: Jan 1, 2022 – Dec 31, 2023
- **Features Used**:  
  - `Date`, `Open`, `High`, `Low`, `Close`, `Adj Close`, `Volume`
- **Target Variable**: `Close` (Closing Price)

---

## 🔍 Objective

To predict the 10th-day closing price using the previous 9 days' closing prices with various RNN-based models and evaluate their performance using MSE (Mean Squared Error).

---

## 🧠 Models Compared

| Model    | Test MSE | Last 10 Days MSE |
|----------|----------|------------------|
| RNN      | 109.07   | **12.32**        |
| LSTM     | 104.94   | 16.49            |
| GRU      | 101.89   | 19.57            |
| Conv1D   | **17.61**| 165.03           |

---

## 📈 Key Observations

- **Conv1D** achieved the **lowest test MSE (17.61)**, indicating strong general performance on the test set.
- **RNN** had the **lowest MSE (12.32)** when predicting the **last 10 days**, showing better short-term generalization.
- **LSTM** and **GRU** performed well but showed moderate overfitting or variance in recent predictions.
- The higher MSE for Conv1D on recent data suggests potential overfitting.

---

## ✅ Conclusion

> While **Conv1D** stands out for minimizing test error, **RNN** appears to better generalize for **short-term (last 10-day) predictions**.

### 📌 Best Overall Model: `Conv1D`  
- Best suited for long-term trend modeling  
- Excellent at minimizing prediction error

### 📌 Best for Short-Term Forecasting: `RNN`  
- Lowest MSE on recent days  
- Good for near-future stock forecasting

---

## 📊 Visual Output

Evaluation graphs are included for all models:
- Training/Test loss trends
- Last 10 predicted vs actual closing prices

![Model Evaluation Sample](graphs/sample-model-comparison.png) <!-- Replace with your actual file path -->

---

## 👩‍💻 Author

**Ruchitha Paccha**  
📧 ruchitha1904@gmail.com  
🔗 [LinkedIn](https://www.linkedin.com/in/ruchitha-chowdary-paccha/)

---

## 🛠️ Tools & Technologies

- Python, Pandas, NumPy
- TensorFlow / Keras
- Matplotlib, Seaborn
- Yahoo Finance API

---

## 📎 How to Run

1. Clone the repository:
```bash
git clone https://github.com/yourusername/stock-price-rnn-models.git
