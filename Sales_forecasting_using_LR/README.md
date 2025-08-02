# 📊 Sales Forecasting with Linear Regression

![Sales Forecast](f487dc30-dbd6-44d0-8229-748095b470cb.png)

## 📌 Project Overview
This project aims to **forecast customer sales using Linear Regression**.  
Businesses often struggle to estimate future sales based on historical data, especially when trends are seasonal.  
By leveraging regression analysis and time-series preprocessing, this project provides **graphical and tabular forecasts** for upcoming sales periods.

---

## 🏆 Problem Statement
Businesses struggle to estimate future sales based on past performance.

---

## 🎯 Objective
- Build a regression model to predict future sales using historical data.  
- Handle seasonal variations and sales differences for improved accuracy.  
- Visualize trends and predictions in an interpretable format.  

---

## 📂 Dataset Description
The dataset used: **`seasonal_sales_dataset.csv`**

| Column  | Type   | Description                         |
|---------|--------|-------------------------------------|
| `date`  | object | Transaction date (2020–2024)        |
| `item`  | object | Item sold                           |
| `store` | object | Store location                      |
| `sales` | int64  | Number of sales                     |

> 📌 Data spans **Jan 2020 – Dec 2024**, with seasonal peaks around November–December to simulate festive sales.

---

## ⚙️ Tech Stack & Libraries
- **Python**  
- **Libraries**  
  - Data Handling: `pandas`, `numpy`  
  - Visualization: `matplotlib`  
  - Machine Learning: `scikit-learn`  
  - Models Tried: `LinearRegression`, `RandomForestRegressor`, `XGBRegressor` 
  - Scaling: `MinMaxScaler`  
  - (Optional) Deep Learning: `LSTM` via `TensorFlow`  

---

## 📈 Methodology
1. **Data Cleaning**
   - Checked for null values  
   - Converted `date` to datetime format  
   - Aggregated daily sales into **monthly sales**

2. **Stationarity Transformation**
   - Calculated sales difference (`sales_diff`) to stabilize trends  

3. **Feature Engineering**
   - Created lag features for the past 12 months  

4. **Train/Test Split**
   - Last 12 months used for testing  
   - Data scaled with `MinMaxScaler`  

5. **Modeling**
   - Applied **Linear Regression**  
   - Predicted monthly sales for the test period  

6. **Evaluation**
   - RMSE: `2908.64`  
   - MAE: `2447.12`  
   - R² Score: `0.4549`  

---

## 📊 Results & Visualizations

### Monthly Customer Sales  
![Monthly Sales](https://github.com/Hariharan-T27/Seasonal-Sales-Forecast/blob/main/Sales_forecasting_using_LR/Outputs/Plots/Monthly%20Customer%20Sales.png)

### Sales Difference (Stationary Data)  
![Sales Difference](https://github.com/Hariharan-T27/Seasonal-Sales-Forecast/blob/main/Sales_forecasting_using_LR/Outputs/Plots/Monthly%20Customer%20Sales%20Difference.png)

### Forecast vs Actual Sales  
![Forecast Plot](https://github.com/Hariharan-T27/Seasonal-Sales-Forecast/blob/main/Sales_forecasting_using_LR/Outputs/Plots/Sales%20Forecast%20using%20LR%20Model.png)

---

## 🚀 How to Run

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/yourusername/sales-forecasting.git
cd sales-forecasting
```

## Install Dependencies
```bash
pip install -r requirements.txt
```
## Run the Project
```bash
python sales_forecast.py
```
## 📂 Project Structure
```bash
├── seasonal_sales_dataset.csv   # Input dataset
├── sales_forecast.py            # Main script
├── outputs/                     # Generated plots
│   ├── monthly_sales.png
│   ├── sales_difference.png
│   └── forecast_plot.png
├── requirements.txt             # Dependencies
└── README.md                    # Documentation
```
## 🔮 Future Enhancements
* Implement advanced ML models (XGBoost, RandomForest)

* Deploy an interactive dashboard (Streamlit/Plotly Dash)

* Incorporate deep learning models (LSTM/GRU) for sequence forecasting

* Add holiday/event impact features to improve festive season accuracy
## 🙌 Acknowledgments
* Libraries: scikit-learn, TensorFlow, XGBoost

* Dataset: Custom-generated seasonal sales data
## Authors

- [@Hariharan-T27](https://github.com/Hariharan-T27)


## Contact
- thariharan76@gmail.

### Requirements 
```bash
pandas==2.2.2
numpy==1.26.4
matplotlib==3.9.0
scikit-learn==1.5.1
xgboost==2.1.1
tensorflow==2.17.0
```
## Contact
- thariharan76@gmail.

### Requirements 
```bash
pandas==2.2.2
numpy==1.26.4
matplotlib==3.9.0
scikit-learn==1.5.1
xgboost==2.1.1
tensorflow==2.17.0
```
