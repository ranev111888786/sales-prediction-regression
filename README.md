\# 📊 Sales Prediction Using Linear Regression \& SGD Regressor  

A machine learning project that develops and evaluates regression models to \*\*predict product sales\*\* using key numerical features such as MSRP, Quantity Ordered, and Price Each.



This project demonstrates the complete machine learning pipeline — from data cleaning and feature selection to model training, evaluation, and optimization.



---



\## 📁 Repository Contents



This repository includes:



\- `sales\_prediction\_.py` → Python script containing the entire workflow for data cleaning, visualization, regression modeling, and evaluation. :contentReference\[oaicite:0]{index=0}

\- `sales\_data\_sample.csv` → Dataset used for modeling. :contentReference\[oaicite:1]{index=1}

\- `sales\_prediction\_report.pdf` → Full academic report explaining the methodology, analysis, and results (17-page project).  



---



\## 🎯 Project Goal



To build a regression model that can predict \*\*SALES\*\* of a product based on:



\- \*\*MSRP\*\*

\- \*\*QUANTITYORDERED\*\*

\- \*\*PRICEEACH\*\*



These features were identified as the strongest predictors for sales after analyzing correlations and visual patterns (see correlation heatmap on \*page 10 of the report\*).



---



\## 🧠 Background \& Context



As covered in the project report (pages 1–3), sales prediction is crucial in:



\- Demand forecasting  

\- Understanding customer behavior  

\- Optimizing pricing  

\- Improving profitability  



The dataset comes from Kaggle and contains \*\*2823 rows and 25 columns\*\*, including order information, product details, customer data, and sales figures.



---



\## 🔍 Data Preparation Workflow



Based on the steps documented in the report (pages 3–9) and implemented in the script:



\### ✔ Step 1 — Remove high-null categorical columns  

Columns with excessive missing values were dropped:



\- `ADDRESSLINE2`

\- `STATE`

\- `TERRITORY`



\### ✔ Step 2 — Remove rows with null POSTALCODE  

76 rows with missing postal codes were removed to maintain data consistency.



\### ✔ Step 3 — Remove duplicates  

This ensures the regression model is not biased by repeated entries.



\### ✔ Step 4 — Select numeric predictor variables  

Feature selection showed strongest numerical predictors:



\- `QUANTITYORDERED`

\- `PRICEEACH`

\- `MSRP`



(See heatmap on \*page 10\* and scatter plots on earlier pages.)



---



\## 📊 Exploratory Data Analysis (EDA)



The notebook performs:



\- Missing value inspection  

\- Summary statistics  

\- Data type inspection  

\- Scatter plots for visual correlations  

\- Correlation matrix \& heatmap  



These plots help justify why the selected features correlate with \*\*SALES\*\*.



---



\## 🤖 Model Development



\### \*\*1️⃣ Scaling\*\*

StandardScaler was applied to normalize:



\- QUANTITYORDERED  

\- PRICEEACH  

\- MSRP  



\### \*\*2️⃣ Train/Test Split\*\*

\- 80% Training  

\- 20% Testing  



\### \*\*3️⃣ Linear Regression Model\*\*

Trained using:



```python

LR = linear\_model.LinearRegression()

LR.fit(X\_train, y\_train)

```



Outputs:



\- Regression coefficients  

\- Intercept  

\- Prediction equation  

\- RMSE  

\- R² Score  

\- Cross-validation score  



\### \*\*4️⃣ SGD Regressor Optimization\*\*

Tested various:



\- Learning rates (`eta0`)

\- Iteration levels (`max\_iter`)



Hyperparameter tuning was performed using \*\*GridSearchCV\*\*.



Best parameters and results appear in the script and the report (page 11–13).



---



\## 📈 Model Performance



From the results in the script and in the report:



| Metric | Value |

|--------|-------|

| \*\*RMSE\*\* | ~487 |

| \*\*R² Score (Linear Regression)\*\* | ~0.92 |

| \*\*Best SGD Regression Score\*\* | -0.213 (indicating underfitting due to small dataset size) |



Cross-validation shows consistent results, strengthening the model's generalizability.



---



\## 📝 Conclusion



As summarized on page 12 of the report:



\- A functional linear regression model was built for predicting sales.

\- MSRP, Quantity Ordered, and Price Each proved to be strong predictors.

\- Prediction accuracy improves with more data — the sample size (2823 rows) limits performance.

\- SGDRegressor requires more tuning and larger datasets to outperform simple linear regression.

\- The dataset supports additional future analysis such as:

&nbsp; - Profit prediction  

&nbsp; - Category-wise forecasting  

&nbsp; - Regional sales modeling  



---



\## 🚀 How to Run This Project



\### 1. Install Dependencies



```bash

pip install numpy pandas seaborn matplotlib scikit-learn plotly

```



\### 2. Run the Python Script



```bash

python sales\_prediction\_.py

```



\### 3. OR open it in Jupyter:



```bash

jupyter notebook

```



---



\## 🧾 References



(As listed in your project report)



\- Kaggle Sales Dataset  

\- DBS Lecture Notes on Linear Regression  

\- Scikit-Learn Documentation  

\- Python for Data Analysis Resources  



---



\## 👨‍💻 Authors



\- Mukesh Kumar  

\- Vaibhav Rane  

\- Yogesh Birajdar  



---

