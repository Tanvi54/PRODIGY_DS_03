# 🛍️ Predicting Repeat Buyers using Decision Tree Classifier

This project focuses on building an **interpretable Decision Tree Classifier** to predict whether a customer will become a **repeat buyer** based on their first purchase behavior, order details, and shopping time patterns.

---

## 📌 Objective
To predict whether a customer will make **more than one purchase** (repeat buyer) based on:
- Order details (quantity, price)
- Shopping time (hour, day of week)
- Geographical location (country)

---

## 🧪 Model Used
- **DecisionTreeClassifier** (`scikit-learn`)
- Maximum depth tuned for interpretability and performance

---

## 📈 Performance
- **Test Accuracy:** ~93.4%  
- **Cross-validated Accuracy:** ~93%  
- **Top Features:**  
  - `CustomerID` (behavior patterns)
  - `Hour` (time of shopping)
  - `DayOfWeek` (shopping day trends)
  - `Country` (geographic influence)

---

## 🔍 Steps Followed

1. **Data Cleaning**
   - Handled missing values (`CustomerID`)
   - Removed irrelevant columns (e.g., descriptions, invoice numbers)

2. **Feature Engineering**
   - Extracted **hour** and **day of week** from timestamps
   - One-hot encoded **country**
   - Created **repeat buyer** label based on order counts

3. **Model Training**
   - Trained a `DecisionTreeClassifier` (max depth = 8)
   - Evaluated with **train-test split** and **cross-validation**

4. **Evaluation**
   - Confusion matrix
   - Classification report
   - Accuracy score

5. **Interpretation**
   - Visualized the tree structure
   - Analyzed **feature importances** to understand customer behavior drivers

---

## 📊 Visualization Example

### Top 10 Feature Importances:
![Feature Importance](path_to_feature_importance_plot.png)

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
