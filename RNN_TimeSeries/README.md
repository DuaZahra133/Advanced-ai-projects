#  Time Series Forecasting with LSTM

## Overview
This project demonstrates a **time series forecasting model** using **LSTM (Long Short-Term Memory)** to predict future stock or weather values based on historical data.  
The project is part of my AI learning portfolio, showcasing skills in **RNNs, LSTM, data preparation, model training, evaluation, and visualization**.

---

## Dataset
- **Dataset:** Apple Stock Price (AAPL) historical data, downloaded from Yahoo Finance.  
- **Columns used:** `Date` and `Close` price.  
- **Rows:** ~500–1000 (subset for faster training on slow laptops).  
- The dataset is provided as `sample_stock.csv` in this repository.  

---

## Tools & Libraries
- **Python 3**  
- **Pandas** – data manipulation  
- **NumPy** – numerical operations  
- **Matplotlib** – visualization  
- **TensorFlow / Keras** – LSTM model  
- **scikit-learn** – RMSE & MAE evaluation metrics  

---

## Project Steps

### 1️⃣ Load & Explore Dataset
- Load CSV and check structure (`head()` & `info()`).  
- Visualize target feature (`Close` price) over time.

### 2️⃣ Prepare Time Series Sequences
- Convert series into supervised learning format:
  - Input: past `sequence_length` timesteps  
  - Output: next timestep value  
- Reshape to `(samples, timesteps, features)` for LSTM.

### 3️⃣ Train/Test Split
- 80% training, 20% testing.  
- Ensures the model learns patterns and evaluates predictions correctly.

### 4️⃣ Build LSTM Model
- Architecture:
  - LSTM layer with 50 units  
  - Dense output layer with 1 unit  
- Optimizer: Adam  
- Loss function: MSE

### 5️⃣ Train Model
- Batch size: 16  
- Epochs: 50  
- Validation data used to monitor performance

### 6️⃣ Evaluate & Visualize
- Predict values on test set  
- Calculate **RMSE** & **MAE**  
- Plot **Actual vs Predicted** to assess model visually

---

## Results
- Model accurately predicts trends in the stock price using past timesteps.  
- Visualization shows predictions following real data trends closely.  
- Evaluation metrics:
  - RMSE: *[2.735339116757426]*  
  - MAE: *[1.7390581538253602]*

