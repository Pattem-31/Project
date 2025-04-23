# Customer Lifetime Value (LTV) Prediction

## Objective
Predict the lifetime value (LTV) of customers based on their purchase behavior to support targeted marketing and strategic customer segmentation.

---

## Tools & Libraries
- **Python**
- **Pandas, NumPy**
- **Scikit-learn, XGBoost, Random Forest**
- **Matplotlib, Seaborn**

---

## Dataset
**WA_Fn-UseC_-Marketing-Customer-Value-Analysis.csv**

This dataset contains customer demographic, policy, and claim-related information.

---

## Features Engineered
- **Recency**: Days since the customer’s last transaction
- **Frequency**: Number of policies
- **AOV** (Average Order Value): `Total Claim Amount / Number of Policies`

---

## Workflow

1. **Data Preprocessing**
   - Parse date columns
   - Handle categorical variables with Label Encoding

2. **Feature Engineering**
   - Compute Recency, Frequency, and AOV

3. **Model Training**
   - Used Random Forest Regressor (optionally XGBoost)
   - Trained on features like Income, Total Claim Amount, etc.

4. **Evaluation**
   - Metrics: MAE, RMSE

5. **Prediction & Segmentation**
   - Predict LTV for all customers
   - Segment customers into `Low`, `Medium`, and `High` value groups based on predicted LTV quantiles

6. **Export**
   - Final predictions and segments saved as `LTV_Predictions_RF.csv`

---

## Visualizations
- Distribution of Customer Lifetime Value
- Feature importance
- Boxplot of LTV by segment
- Scatter plot of Total Claim vs Predicted LTV
- Violin plot of AOV by segment
- Correlation heatmap
- Average Income by LTV segment

---

## Output
- Python notebook/script (`.ipynb` or `.py`)
- Trained model
- Visualizations
- `LTV_Predictions_RF.csv` with predicted LTVs and segments

---

## How to Run

```bash
pip install pandas numpy scikit-learn xgboost matplotlib seaborn
python ltv_prediction.py
