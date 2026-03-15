# AI-Based Return Fraud Detection System

## Overview
This project is an AI-powered fraud detection system designed to identify suspicious return requests in e-commerce platforms. The system analyzes customer return behavior, refund patterns, and risk indicators using a machine learning model to estimate the probability of fraudulent activity.

The solution provides a simple dashboard interface that allows analysts to input return details and instantly receive a fraud risk prediction.

---

## Features

- Machine Learning-based fraud prediction
- Real-time API using FastAPI
- Interactive fraud risk dashboard
- Animated fraud risk gauge
- Fraud alert indicator
- Input validation and reset functionality
- Random test case generator for demo
- Explanation of risk factors

---

## Technologies Used

### Backend
- Python
- FastAPI
- Scikit-Learn
- Pandas
- NumPy
- Joblib

### Frontend
- HTML
- CSS
- JavaScript
- Canvas API

### Machine Learning
- Random Forest Classifier

---

## System Architecture

User Input → FastAPI Backend → ML Model → Fraud Probability → Dashboard Visualization

---

## Folder Structure
Return_Fraud_Detection
│
├── backend
│ ├── main.py
│ ├── requirements.txt
│ └── model
│ ├── generate_data.py
│ ├── train_model.py
│ ├── fraud_dataset.csv
│ └── fraud_model.pkl
│
├── frontend
│ ├── index.html
│ ├── script.js
│ └── style.css
│
├── firebase
│ └── firebase_config.js
│
└── README.md


---

## Dataset Generation

Synthetic transaction data is generated to simulate real-world return behaviors including:

- number of returns
- refund amount
- time gap between purchase and return
- product mismatch indicator
- product category risk
- customer loyalty score
- return reason pattern

Dataset size: **20,000 records**

---

## Model Training

A Random Forest classifier is trained to predict fraud probability.

Example features used:

- return frequency
- refund value
- return timing
- mismatch detection
- category risk
- loyalty score

---

## How to Run the Project

### 1 Install dependencies
pip install -r backend/requirements.txt


### 2 Generate dataset


cd backend/model
python generate_data.py


### 3 Train model


python train_model.py


### 4 Start backend server

cd backend
uvicorn main:app --reload


Server runs at:


http://127.0.0.1:8000


### 5 Open dashboard

Open:


frontend/index.html


in a browser or with Live Server.

---

## Example Prediction

Input example:


Returns: 6
Refund: 4200
Time gap: 2
Mismatch: 1
Category risk: 4
Loyalty: 3


Output:


Fraud Score: 82%
Prediction: FRAUD
⚠ FRAUD ALERT


---

## Future Improvements

- Real transaction dataset integration
- Model explainability using SHAP
- User authentication
- Fraud monitoring dashboard for multiple transactions
- Cloud deployment

---

## Team

**Team Name:** NexaTech

Members:
- Shravani Mahesh Dhore (Team Leader)
- Purva Pendbhaje
- Rutuja Yadav

Program:
M.Sc Data Science & Big Data Analytics  
MIT-WPU, Pune