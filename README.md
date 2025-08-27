# 🏠 Energy Efficiency – LightGBM Regression

This project focuses on the **Energy Efficiency dataset** (UCI / Kaggle).  
The goal is to predict **Heating Load (Y1)** and **Cooling Load (Y2)** of buildings using supervised learning methods, with a primary focus on **LightGBM Regressor**.

---

## 📂 Dataset
- **Features (X1–X8):**
  - Compactness
  - Surface
  - Wall
  - Roof
  - Height
  - Orientation
  - Glazing
  - Glazing Distribution
- **Targets:**
  - HeatingLoad (Y1)
  - CoolingLoad (Y2)

The dataset contains **768 observations** with no missing values.

---

## 🔍 Project Workflow
1. **Data Preparation**
   - Renamed columns for readability (X1→Compactness, …, Y1→HeatingLoad).
   - Train-test split (80/20).

2. **Baseline Model**
   - Trained a default **LGBMRegressor**.
   - Evaluated with R² and RMSE metrics.

3. **Hyperparameter Tuning**
   - Used **RandomizedSearchCV** with 5-fold CV.
   - Tuned parameters: `num_leaves`, `max_depth`, `learning_rate`, `n_estimators`,  
     `min_child_samples`, `subsample`, `colsample_bytree`, `reg_alpha`, `reg_lambda`.

4. **Final Evaluation**
   - Reported best parameters, CV best RMSE, and test scores (R², RMSE).
   - Optionally repeated for **Cooling Load**.

---

## 📊 Results
- Baseline LGBM achieved strong performance.  
- Hyperparameter tuning further improved RMSE and R².  
- Heating and Cooling Load prediction can be modeled effectively with gradient boosting.

---

## 🚀 Tech Stack
- Python 3
- pandas, numpy
- scikit-learn
- lightgbm
- matplotlib / seaborn (EDA & visualization)

---

## 📌 How to Run
```bash
# Clone the repo
git clone https://github.com/yourusername/energy-efficiency-lgbm.git
cd energy-efficiency-lgbm

# Install dependencies
pip install -r requirements.txt

# Run Jupyter Notebook
jupyter notebook
