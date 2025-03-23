# 🦠 COVID-19 Death Analysis and Prediction

This project analyzes and predicts COVID-19-related deaths across the United States using a dataset spanning from 2020 to 2023. It involves thorough data preprocessing, visualization, and the application of machine learning and deep learning models.

## 📊 Dataset Overview

**Source:** [Data.gov - CDC](https://catalog.data.gov/dataset/conditions-contributing-to-deaths-involving-coronavirus-disease-2019-covid-19-by-age-group)  
**Total Records:** 621,000  
**Key Features:**
- **Demographics:** State, Age Group
- **Time Period:** Start Date, End Date
- **Medical Conditions:** Condition Group, Condition, ICD10 Codes
- **Metrics:** COVID-19 Deaths, Number of Mentions

**Missing Values:**
- Year: 12,420 entries
- Month: 62,100 entries
- COVID-19 Deaths: 183,449 entries
- Number of Mentions: 177,577 entries

---

## ⚙️ Preprocessing

- **Missing Values:**
  - Year & Month: Filled using the mode
  - Deaths & Mentions: Filled using the median
- **Dropped:** `Flag` column (70% missing)
- **Encoding:** Label Encoding for categorical variables
- **Scaling:** Min-Max Scaling applied to numerical features
- **Outlier Handling:** Boxplot + IQR method for removal

---

## 📈 Visualizations

- **Correlation Heatmap**
- **COVID-19 Death Distribution** (Highly skewed)
- **Monthly Death Trends**
- **Deaths by Age Group** (Higher in older age groups)
- **Deaths by State** (Certain states had disproportionately higher deaths)

---

## 🧠 Machine Learning Models

| Model             | R² Score | MSE     | Time (s) |
|------------------|----------|---------|----------|
| Ridge Regression | 0.946    | 0.002   | 0.031    |
| Gradient Boosting| 0.993    | 0.0003  | 16.94    |
| Random Forest    | 0.996    | 0.0001  | 24.43    |
| Neural Network   | 0.994    | 0.0002  | 65.00    |

### ✅ Best Performing Models:
- **Random Forest**, **Gradient Boosting**, and **Neural Network** performed comparably well
- **Ridge Regression** had the weakest performance

---

## 🧬 Neural Network Architecture

- **Input:** Preprocessed features
- **Hidden Layers:** 64 → 32 neurons (ReLU activation)
- **Output:** Predicted COVID-19 Deaths
- **Loss Function:** Mean Squared Error (MSE)
- **Optimizer:** Adam

---

## 📚 References

- **Preprocessing Techniques:** Little & Rubin (2019), Scikit-learn docs
- **Outlier Detection:** Iglewicz & Hoaglin (1993)
- **ML Algorithms:** Breiman (2001), Friedman (2001), Goodfellow et al. (2016)
- **Evaluation Metrics:** Willmott & Matsuura (2005)
- **Visualization Tools:** Matplotlib, Seaborn

---

## 📌 Conclusion

This study highlights the effectiveness of ensemble and deep learning models for predicting COVID-19-related deaths using publicly available data. With proper preprocessing and feature handling, high prediction accuracy can be achieved.

---

## 💻 Technologies Used

- Python
- Pandas, NumPy
- Scikit-learn
- PyTorch
- Seaborn, Matplotlib

---

## 📎 License

This project is open-source and available under the [MIT License](LICENSE).

