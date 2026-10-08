# 🏠 House Price Prediction Model

This project predicts house prices using **Linear Regression** based on various features such as lot area, building type, overall condition, year built, and basement area.

---

## 📌 Project Overview
The dataset contains house attributes and target sale prices. The model undergoes data cleaning, handling missing values, categorical encoding, feature scaling, and evaluation using standard regression metrics.

---

## 📊 Dataset Details

The dataset `HousePricePrediction.csv` consists of the following key features:

- **Id**: Unique identification for each record (dropped during preprocessing)
- **MSSubClass**: Identifies the type of dwelling
- **MSZoning**: General zoning classification
- **LotArea**: Lot size in square feet
- **LotConfig**: Lot configuration
- **BldgType**: Type of dwelling
- **OverallCond**: Rates the overall condition of the house
- **YearBuilt**: Original construction date
- **YearRemodAdd**: Remodel date
- **Exterior1st**: Exterior covering on house
- **BsmtFinSF2**: Type 2 finished square feet
- **TotalBsmtSF**: Total square feet of basement area
- **SalePrice**: Target variable (Price of the house)

---

## 🛠️ Project Workflow

1. **Data Loading & Exploration**:
   - Inspected shape, columns, missing values, and data types.
2. **Data Preprocessing**:
   - Dropped unwanted columns (`Id`).
   - Handled missing values (`SalePrice` missing values filled with the mean; remaining null rows dropped).
3. **Categorical Encoding**:
   - Applied One-Hot Encoding (`pd.get_dummies`) on columns like `MSZoning`, `LotConfig`, `BldgType`, and `Exterior1st`.
4. **Train-Test Split**:
   - Split the dataset into training (80%) and testing (20%) sets.
5. **Model Training & Feature Scaling**:
   - Trained a `LinearRegression` model.
   - Applied `StandardScaler` to evaluate baseline performance improvements.

---

## 📈 Model Performance Metrics

| Metric | Score (Baseline) | Score (Scaled) |
| :--- | :--- | :--- |
| **R² Score** | `0.3741` | `0.3741` |
| **MAE** | `30,829.94` | `30,829.94` |
| **RMSE** | `41,138.56` | `41,138.56` |
| **MAPE** | `18.74%` | `18.74%` |

---

## 🚀 How to Run

1. Clone or download this repository.
2. Ensure you have Python installed along with the required libraries:
   ```bash
   pip install pandas numpy scikit-learn matplotlib
