# Used Car Price Prediction

## 📌 Overview
This project predicts the market price of used vehicles using machine learning techniques.  
We perform exploratory data analysis (EDA), feature engineering, and model evaluation on the [Kaggle Vehicles Dataset](https://www.kaggle.com/datasets/austinreese/craigslist-carstrucks-data).

The workflow includes:
- Cleaning and preprocessing 50+ features (numeric, categorical, boolean)
- One-hot encoding for categorical variables
- Outlier removal and data filtering
- Model training & evaluation with multiple algorithms
- Model performance comparison

---

## 📊 Dataset
- **Source:** [Kaggle - Craigslist Vehicles Dataset](https://www.kaggle.com/datasets/austinreese/craigslist-carstrucks-data)
- **Rows:** ~58,000 after cleaning
- **Columns:** 98 (after encoding)
- **Target:** `price`

---

## 🛠️ Tech Stack
- Python 3.x  
- Pandas, NumPy  
- Matplotlib, Seaborn (EDA & visualization)  
- Scikit-learn (Linear Regression, Lasso, Random Forest)  
- XGBoost (gradient boosting)  

---

## 📈 Exploratory Data Analysis (EDA)
Some key findings:
- **Negative correlation** between odometer mileage and price.
- **Positive correlation** between newer car year and price.
- Trucks and pickups tend to have higher average prices.
- Price distribution is heavily skewed, requiring filtering.

**Example visualizations:**
- Price vs. Odometer scatter plots
- Price distribution histograms
- Average price by car type bar charts
- Correlation heatmaps

---

## 🧮 Models & Results

| Model                  | MAE ($)  | RMSE ($) | R²     |
|------------------------|----------|----------|--------|
| Linear Regression      | 5,659.64 | 8,025.42 | 0.6857 |
| Lasso Regression       | 5,657.26 | 8,025.42 | 0.6857 |
| Random Forest          | 4,470.15 | 6,717.85 | 0.7798 |
| **XGBoost**            | **4,068.92** | **6,295.51** | **0.8066** |

> XGBoost achieved the best overall performance with the lowest error and highest R² score.

---

## 🚀 How to Run
```bash
# Clone the repository
git clone https://github.com/<your-username>/used-car-price-prediction.git
cd used-car-price-prediction

# Install dependencies
pip install -r requirements.txt

# Run Jupyter Notebook
jupyter notebook ProjectProposal.ipynb

