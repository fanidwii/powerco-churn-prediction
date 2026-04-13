# PowerCo SME Customer Churn Prediction

## 📌 Project Overview
This project is part of the BCG Data Science simulation on Forage. The objective is to investigate the factors driving customer churn for PowerCo, a major gas and electricity utility company supplying small and medium-sized enterprises (SMEs). 

The primary hypothesis from the client was that **price sensitivity** is the main driver of customer churn. This project involves end-to-end data analysis, feature engineering, and the development of a predictive Machine Learning model to test this hypothesis and provide actionable business recommendations.

## 💼 Business Problem
The energy market has become increasingly competitive, leading to an alarming churn rate among PowerCo's SME customers. PowerCo management assumes that customers are leaving for competitors solely due to better pricing. We need to:
1. Verify if price sensitivity is the critical factor for churn.
2. Build a predictive model to identify customers at high risk of churning.
3. Recommend a data-driven retention strategy.

## 🛠️ Methodology & Tech Stack
- **Language:** Python
- **Libraries:** Pandas, NumPy, Matplotlib, Seaborn, Scikit-Learn
- **Workflow:**
  1. **Exploratory Data Analysis (EDA):** Visualizing data distribution, handling skewed consumption data, and exploring churn rates against customer tenure.
  2. **Feature Engineering:** Extracting actionable features from raw date columns (e.g., `tenure` in months) and creating a specific "Price Sensitivity" metric by calculating the difference between December and January off-peak prices.
  3. **Predictive Modeling:** Training a **Random Forest Classifier** with balanced class weights to handle the highly imbalanced churn dataset.

## 📊 Key Findings & Business Impact
1. **The Price Sensitivity Myth:** While price fluctuations do play a role, our Random Forest model revealed that it is **not the main driver** of churn.
2. **Top Predictors:** The most influential factors dictating churn are the customer's **Net Margin** and **Annual Energy Consumption**.
3. **Model Performance:** The Random Forest model achieved a **Precision of 79%**. 
    * *Business Value:* This means when the model predicts a customer will churn, it is correct 79% of the time. PowerCo can confidently offer targeted 20% retention discounts to these specific high-risk customers, avoiding the massive revenue loss of applying blind, mass discounts to loyal customers.

## 📂 Repository Structure
* `client_data.csv` - Historical customer usage, margins, and contract data.
* `price_data.csv` - Historical variable and fixed pricing data.
* `main.py` - The complete Python script containing EDA, feature engineering, and the Random Forest model implementation.

## 🚀 How to Run the Code
1. Clone this repository:
   ```bash
   git clone https://github.com/fanidwii/powerco-churn-prediction.git
