# Telecom Churn Prediction — MLOps Pipeline

Predicts which telecom customers will churn, using the IBM Telco Customer Churn dataset (7,043 customers).

## Stack
scikit-learn · MLflow · FastAPI · Streamlit · Docker · GitHub Actions · Render + Streamlit Cloud

## Live demo
- API: https://churn-mlops-dazf.onrender.com/docs
- UI: https://churn-mlops-app.streamlit.app/

## Run locally
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
python src/train.py
uvicorn main:app --app-dir api --reload   # in one terminal
streamlit run dashboard.py                # in another

## Results
Logistic Regression: ROC-AUC = 0.8416 (best model, auto-selected)
Random Forest: ROC-AUC = 0.8220

<img width="749" height="562" alt="image" src="https://github.com/user-attachments/assets/3ce7ca1a-d7c0-434a-8060-0f251f6f05a2" />
