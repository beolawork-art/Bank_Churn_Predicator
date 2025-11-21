# 🏦 Bank Customer Churn Prediction & Retention Model

**Project Status: Completed**

---

This project focuses on building a machine learning solution to help a retail bank proactively identify customers who are at a **high risk of churning (leaving)**. 
By accurately predicting churn, the bank can target these customers with specific, timely retention offers, significantly reducing customer loss.

| Metric | Result |
| :--- | :--- |
| **Final Accuracy** | **86%** |
| **Churn Recall Rate (Detection)** | **46%** (Focusing on finding customers most likely to leave) |
| **Model** | Random Forest Classifier |

---

## 🛠️ Methodology & Technical Stack

The entire analysis, from Exploratory Data Analysis (EDA) to model deployment readiness, was conducted using a robust Python pipeline.

### Tools and Libraries

* **Python 3.10**
* **Data Manipulation:** `Pandas`, `NumPy`
* **Modeling:** `Scikit-learn` (RandomForestClassifier, GridSearchCV, pipeline)
* **Visualization:** `Matplotlib`, `Seaborn`
* **Environment Management:** `Conda`

### Key Steps in the Pipeline

1.  **Exploratory Data Analysis (EDA):** Identified key correlations, reviewed distributions, and handled missing values.
2.  **Feature Engineering:** Created new features (e.g., ratios of balance to salary) to enhance predictive power.
3.  **Data Preprocessing:** Handled categorical variables using One-Hot Encoding and scaled numerical features (StandardScaler).
4.  **Handling Imbalance:** Applied SMOTE (Synthetic Minority Over-sampling Technique) to address the low percentage of churned customers in the training data.
5.  **Model Training:** Trained and tuned a **Random Forest Classifier**, optimizing for the **Recall** metric, which is critical for finding as many potential churners as possible.

6.  ---

## 🔎 Key Findings & Business Impact

### Feature Importance

The analysis clearly identified the key features driving customer churn. **The strongest predictors were centered around customer relationship length, service usage, and financial behavior.**

<img width="609" height="468" alt="download" src="https://github.com/user-attachments/assets/d5743549-0cae-436a-9c98-615caa949ab1" />
<img width="636" height="468" alt="download" src="https://github.com/user-attachments/assets/64aad2c5-3334-4ec7-8a1d-57a8dad4e7d4" />

| Top 3 Churn Predictors | Impact |
| :--- | :--- |
| **[Feature 1 - e.g., High Account Balance]** | Customers with higher balances and no additional services showed higher instability. |
| **[Feature 2 - e.g., Older Age Group]** | Older customer groups appeared less loyal compared to middle-aged groups. |
| **[Feature 3 - e.g., Tenure (Short Time as Customer)]** | New customers are highly volatile and pose an immediate risk. |

### Model Performance

,Predicted: Stayed (0),Predicted: Left (1),Total
Actual: Stayed (0),"1,543 (TN)",64 (FP),"1,607"
Actual: Left (1),212 (FN),181 (TP),393

<img width="658" height="545" alt="download" src="https://github.com/user-attachments/assets/f959f3dd-df8a-4693-af54-a3eb15782328" />

The model's high **Recall of 46%** means that the bank can now detect almost half of the customers who are going to leave, providing a huge advantage in their retention efforts compared to random guessing.

---

## 🚀 How to Run the Project

To replicate this analysis, please follow these steps:

1.  **Clone the repository:**
    ```bash
    git clone (https://github.com/beolawork-art/Bank_Churn_Predicator)
    ```
2.  **Create and activate the Conda environment:**
    ```bash
    conda create --name bank_churn_env python=3.10
    conda activate bank_churn_env
    ```
3.  **Install dependencies:**
    ```bash
    conda install pandas numpy scikit-learn matplotlib seaborn jupyter
    ```
4.  **Launch Jupyter:**
    ```bash
    jupyter notebook
    ```
5.  Open the main analysis notebook: **`Bank_Customer_Churn_Prediction.ipynb`** and run the cells sequentially.

---

**Project Contributor:** Olaitan Bello
**Contact:** beola.work@gmail.com
