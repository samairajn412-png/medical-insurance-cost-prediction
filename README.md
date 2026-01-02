# **Medical Insurance Cost Prediction**

## **Overview**
This mini machine learning project predicts **medical insurance charges** based on personal and health-related features like age, BMI, number of children, smoking status, gender, and region.  

It demonstrates **data preprocessing, feature engineering, encoding, scaling, transformations, and model comparison** for regression.

---

## **Dataset**
- Source: Publicly available insurance dataset (`insurance.csv`)  
- Features:
  - `age` – Age of the individual
  - `sex` – Gender (`male`/`female`)
  - `bmi` – Body Mass Index
  - `children` – Number of children
  - `smoker` – Smoking status (`yes`/`no`)
  - `region` – Residential area
  - `charges` – Medical insurance charges (target)

---

## **Notebooks**
### **Notebook 1 – Data Understanding & Cleaning**
- Explored dataset using `head()`, `info()`, `describe()`
- Identified numerical vs categorical columns
- Depicted correlation among columns
- Removed duplicates
- Performed univariate analysis with basic conclusions

### **Notebook 2 – Exploratory Data Analysis**
- Visualized categorical features (`countplot`, `pie charts`)
- Visualized numerical features (`histogram`, `distplot`, `boxplot`)
- Bivariate analysis: scatter plots, bar plots, boxplots, pairplots
- Observed relationships between features and target

### **Notebook 3 – Feature Transformations & Encoding**
- Applied **scaling** (`StandardScaler`) and **Power Transform** on numerical columns
- Log-transform of target to improve regression
- Created **interaction features** (`smoker*bmi`, `smoker*age`)
- One-hot encoding of categorical variables
- Observed effect of each transformation step on CV R²
- Markdown explanations for why some transformations improve performance, others don’t

### **Notebook 4 – Outlier Handling & Model Comparison**
- Visualized outliers in target (`charges`) using boxplots
- Compared models with and without outlier removal
- Applied log-transform and scaling
- Compared multiple regression models:
  - Linear Regression, Ridge, Lasso, Random Forest
  - Observed CV R² scores at each step
- Random Forest achieved the **best accuracy**, capturing non-linear relationships and interactions

---

## **Key Learnings**
- Feature scaling and transformations may not always improve linear models if interactions or non-linearities exist.
- Tree-based models like **Random Forest** naturally capture interactions and non-linear relationships.
- Outlier handling should be visualized and explained; sometimes removing outliers can reduce accuracy.
- Proper encoding of categorical variables (One-Hot or Ordinal) can significantly impact performance.

---

## **Repository Structure**
medical_cost_prediction_ML/
├── data/
│ └── insurance.csv
├── notebooks/
│ ├── 01_data_understanding_cleaning.ipynb
│ ├── 02_univariate_bivariate_analysis.ipynb
│ ├── 03_feature_scaling_encoding.ipynb
│ └── 04_outlier_handling_model_comparison.ipynb
├── README.md
└── insurance.zip

---

## **How to Run**
1. Clone the repository:
```bash
git clone https://github.com/samairajn412-png/medical-insurance-cost-prediction.git
