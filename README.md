# AI/ML Internship — Project Tasks

---

## Task 1 — Exploring and Visualizing the Iris Dataset

### Objective
Perform comprehensive exploratory data analysis (EDA) and visualization on the classic Iris dataset to uncover patterns and relationships between flower species and their physical measurements.


### Models / Techniques Applied
- Univariate analysis — histograms, box plots
- Bivariate analysis — scatter plots, violin plots
- Multivariate analysis — pair plot with KDE
- Correlation heatmap
- Per-species statistical summaries

### Key Results & Findings
- **Iris setosa** is completely linearly separable from the other two species using petal dimensions alone
- **Petal length** and **petal width** are the most discriminating features (correlation ~0.96)
- **Sepal width** shows the weakest inter-species separation
- *Versicolor* and *virginica* overlap slightly but remain mostly distinguishable
- Dataset is clean — zero missing values, perfectly balanced classes (50 each)

---

## Task 2 — Predicting Future Stock Prices (Short-Term)

### Objective
Use historical OHLCV (Open, High, Low, Close, Volume) stock data along with engineered technical features to predict the **next day's closing price** using regression models.

### Models Applied
| Model | Description |
|-------|-------------|
| Linear Regression | Baseline model, interpretable coefficients |
| Random Forest Regressor | Ensemble model, captures non-linear patterns |

### Feature Engineering
- Lag features: `Close_Lag1`, `Close_Lag2`, `Volume_Lag1`
- Rolling statistics: 5-day & 10-day moving averages, 5-day std deviation
- Derived: Price range (High−Low), price change (Close−Open), % daily change


---

## Task 3 — Heart Disease Prediction

### Objective
Build and evaluate binary classification models to predict whether a patient is at risk of heart disease based on clinical measurements from the UCI Heart Disease dataset.


### Models Applied
| Model | Description |
|-------|-------------|
| Logistic Regression | Linear probabilistic classifier, highly interpretable |
| Decision Tree | Rule-based, visualizable decision boundaries |
| Random Forest | Ensemble method for best accuracy + feature importance |

### Evaluation Metrics
- Accuracy, Precision, Recall, F1-Score
- ROC Curve & AUC Score
- Confusion Matrix

**Top Predictive Features:**
1. `thal` — Thalassemia type (reversible defect = high risk)
2. `cp` — Chest pain type (asymptomatic = paradoxically highest risk)
3. `ca` — Number of major vessels (more = higher risk)
4. `thalach` — Max heart rate (lower = higher risk)
5. `oldpeak` — ST depression (higher = worse prognosis)

**Clinical Insights:**
- Male patients show significantly higher disease rates in this dataset
- Asymptomatic chest pain (cp=3) is the most dangerous type
- Exercise-induced angina is a strong positive disease indicator

-

## 🛠️ Setup & Installation

```bash
# Clone the repository
git clone https://github.com/uzair-khiiba/MLTasks-Intern

# Install dependencies
pip install numpy pandas matplotlib seaborn scikit-learn
