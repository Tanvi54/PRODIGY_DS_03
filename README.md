# 🛍️ Predicting Customer Purchase Behavior Using Decision Trees

## 📌 Project Overview
This project builds a **Decision Tree Classifier** to predict whether a customer will make a repeat purchase based on their **demographic** and **behavioral** data.  
The focus is on **interpretable modeling** using features derived from **first purchase behavior**, making the predictions actionable for e-commerce businesses.

---

## **Dataset**
- **Source:** Kaggle E-commerce Transactions Dataset  
- **Features:**  
  - **Behavioral:** Basket size (`Quantity`), average item price (`UnitPrice`), time of purchase (`Hour`), day of week (`DayOfWeek`)  
  - **Demographic:** Customer country (one-hot encoded)
- **Target:** `Purchased` → 1 if the customer made a repeat purchase, 0 otherwise.

---

## 🔍**Project Workflow**
1. **Data Preprocessing:**
   - Removed cancellations & negative quantities.
   - Selected only **first purchase per customer**.
   - Created binary label (`Purchased`) based on future purchases.
2. **Feature Engineering:**
   - Extracted **purchase time** (`Hour`) and **day of week** (`DayOfWeek`).
   - Encoded **country** as categorical variables.
3. **Modeling:**
   - Trained a **Decision Tree Classifier** (`max_depth=6`) for interpretability.
4. **Evaluation:**
   - Accuracy: **~65%**
   - Cross-validated accuracy: **~64–65%**
5. **Insights:**
   - **Unit price** and **purchase time** are the strongest predictors.
   - **Basket size** and **purchase day** also influence repeat purchase behavior.
6. **Visualization:**
   - Feature importance bar chart.
   - Decision tree plot for interpretability.

---

## **Key Insights**
- Customers who spend more per item or buy at certain times are **more likely to return**.
- Behavioral features dominate demographic factors in predicting repeat purchase.

---

## **Technologies Used**
- **Python** (Pandas, NumPy, Matplotlib, Seaborn)
- **Scikit-learn** (DecisionTreeClassifier, train_test_split, cross_val_score)
- **Jupyter Notebook** for interactive analysis

---

## 📈**Results**
- **Accuracy:** ~65%
- **Cross-validation:** ~64–65%
- Balanced performance and interpretable insights for e-commerce strategy.

---

## 🛠️ Tech Stack
- **Python**
- **Pandas**
- **Scikit-learn**
- **Matplotlib**
- **Seaborn**

---

## 🚀 How to Run
```bash
git clone https://github.com/yourusername/repeat-buyer-prediction
cd repeat-buyer-prediction
pip install -r requirements.txt
python main.py
