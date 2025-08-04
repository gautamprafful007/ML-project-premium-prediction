<h1>🧠 ML Project: Health Insurance Premium Prediction.</h1>

A machine learning project that predicts health insurance premiums using user features such as age, BMI, smoker status, etc.
Based on Codebasics ML course workflows 

<h2>📁 Project Structure</h2>

Copy<br>
Edit<br>
├── main.py<br>
├── prediction_helper.py<br>
├── requirements.txt<br>
├── artifacts/             # (optional) trained models, scalers<br>
└── README.md<br>

<h2>🚀 Getting Started</h2>

<li>Clone the repository</li>

bash<br>
Copy<br>
Edit<br>
git clone https://github.com/gautamprafful007/ML-project-premium-prediction.git<br>
cd ML-project-premium-prediction<br>

<li>Install dependencies</li>

bash<br>
Copy<br>
Edit<br>
pip install -r requirements.txt<br>


<h2>🧪 Overview of the Workflow</h2>

<li>Data Loading & Exploration</li>

Load the dataset (e.g., insurance.csv) containing features: age, sex, bmi, children, smoker, region, and target charges.
Perform exploratory data analysis (EDA):
Check null values and duplicates<br>
Plot distributions (pie charts, box plots, scatter plots) to understand feature-target relationships (e.g., smokers vs premium) 

<li>Preprocessing</li>

Encode categorical variables: sex, smoker, region as numeric labels.<br>
Detect and handle outliers (e.g., in BMI using IQR and capping)<br>
Scale and normalize numerical features if necessary.<br>

<li>Feature Engineering</li>

Correlation analysis to identify features most impacting the charges.
Final selection of relevant input features (e.g., age, sex, BMI, smoker) 

<li>Model Development & Evaluation</li>

Split data into training and test sets (e.g., 80/20).
Train multiple ML models:<br>
Linear Regression, Decision Tree, Random Forest, XGBoost, KNN, Gradient Boosting.
Compare performance using metrics like RMSE and R².<br>
Select the best-performing model (often Random Forest or XGBoost) 

<li>Prediction Helper (prediction_helper.py)</li>

Contains functions:
preprocess_input(): encodes and scales new user input.
predict_premium(): loads the trained model and outputs premium prediction.
Optional risk scoring or auxiliary processing logic.

<li>Main Script (main.py)</li>

Integrates data flow:
Load model and helper.
Accept input values (e.g., via CLI or a simple UI).
Use helper functions to preprocess and predict.
Display output premium estimate.

<h2>🛠️ Run & Test the Script</h2>

bash<br>
Copy<br>
Edit<br>
python main.py<br>
You can supply a test input dictionary like:

python<br>
Copy<br>
Edit
{
  "age": 30,
  "sex": "male",
  "bmi": 28.0,
  "children": 1,
  "smoker": "no",
  "region": "northeast"
}
It will preprocess and return the predicted premium amount.

<h2>📊 Results & Insights</h2>

Visualizations help understand how features like smoking status or BMI impact insurance cost.
Correlation analysis confirms strong association particularly of smoker with charges (~0.78 correlation) 
Model evaluations typically show Random Forest or XGBoost outperform others in RMSE and R² metrics.

<h2>🔋 Future Enhancements</h2>

Expand feature space: include more inputs (e.g., medical history, insurance type).
Use more advanced preprocessing (e.g., missing value imputation, polynomial features).
Convert into a web app (Flask/Streamlit) and deploy (e.g. Heroku) for real-time interactivity.
Provide confidence intervals or future cost trends based on user’s health change trajectory.

<h2>🧾 Requirements</h2>

Listed in requirements.txt:

pandas, numpy

scikit-learn

matplotlib, seaborn

(If used) xgboost, feature_engine, pickle, flask

<h2>📜 License</h2>

Licensed under Apache‑2.0 (as seen in the upstream project) 

<h2>✉️ Acknowledgments</h2>

Inspired by the Codebasics ML Course health insurance prediction example 

Study materials and references from related tutorials on insurance premium prediction using Python ML workflows
