# Thyroid Disease Prediction and Deployment using Machine Learning

## 📌 Project Overview
Thyroid disease is a prevalent medical condition that affects metabolic regulation. This project aims to predict the risk of thyroid disease using classical machine learning techniques. The solution follows a modular, scalable, and maintainable approach while leveraging cloud deployment and AI Ops methodologies.

## 📁 Project Structure
```
├── data/                     # Dataset storage
├── notebooks/                # Jupyter notebooks for EDA & modeling
├── src/                      # Source code for model pipeline
│   ├── data_preprocessing.py  # Data cleaning & transformation
│   ├── feature_engineering.py # Feature selection & engineering
│   ├── model_training.py      # ML model training
│   ├── model_evaluation.py    # Model performance evaluation
│   ├── api.py                 # Flask/FastAPI API for predictions
├── tests/                    # Unit & integration tests
├── logs/                     # Application logs
├── requirements.txt          # Python dependencies
├── Dockerfile                # Containerization setup
├── README.md                 # Project documentation
└── config.yaml               # Configuration file for settings
```

## 🚀 Project Workflow & Execution
### 1️⃣ **Data Handling (Cassandra Database - Astra)**
- Connect to **Astra Cassandra DB**.
- Load the thyroid dataset into Cassandra.
- Perform **data cleaning & preprocessing**.

### 2️⃣ **Feature Engineering & Model Training**
- Perform **feature selection** using correlation & SHAP values.
- Train multiple models:
  - Logistic Regression
  - Decision Trees
  - Random Forest
  - XGBoost
  - Support Vector Machines
- **Hyperparameter tuning** for optimal performance.

### 3️⃣ **Model Evaluation & Optimization**
- Evaluate models using:
  - Accuracy, Precision, Recall, F1-score, and ROC-AUC.
- Measure **latency (response time)** for predictions.
- Optimize model for **speed & accuracy trade-offs**.

### 4️⃣ **API Development & Deployment**
- Develop an API using **Flask/FastAPI**.
- Expose endpoints for model inference.
- Containerize using **Docker**.
- Deploy on **AWS/GCP/Azure**.

### 5️⃣ **Logging & Monitoring**
- Implement **Python logging** for tracking system events.
- Monitor performance using **MLflow/DVC**.

### 6️⃣ **AI Ops Pipeline & CI/CD**
- Integrate **DVC for dataset versioning**.
- Use **Jenkins/CircleCI** for automation.
- Deploy via **AWS SageMaker/Azure ML Studio**.

### 7️⃣ **System Design Documentation**
- **HLD (High-Level Design)**: Architecture & data flow.
- **LLD (Low-Level Design)**: Code-level design.
- **Wireframes & System Architecture Documents**.

## 🌐 API Endpoints
| Method | Endpoint | Description |
|--------|---------|-------------|
| POST   | `/predict` | Predicts thyroid risk based on input features |
| GET    | `/health` | Health check for API service |

## 🛠️ Installation & Setup
1. Clone the repository:
   ```bash
   git clone https://github.com/RAHULJOGI-CODE/Thyriod_Detection_Using_ML/
   cd thyroid-prediction
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run API locally:
   ```bash
   python src/api.py
   ```

## 📜 Deployment Instructions
- Use Docker for containerization:
  ```bash
  docker build -t thyroid-prediction .
  docker run -p 5000:5000 thyroid-prediction
  ```
- Deploy on **AWS Lambda / GCP Cloud Run / Azure App Services**.

## 🧪 Testing
- Run unit tests:
  ```bash
  pytest tests/
  ```
- Validate API with Postman or Curl:
  ```bash
  curl -X POST http://127.0.0.1:5000/predict -d '{"TSH": 2.5, "T3": 1.9, "T4": 5.4}' -H "Content-Type: application/json"
  ```

## 🔍 Performance Metrics
- **Model Accuracy:** XX%
- **Precision & Recall:** XX, XX
- **Response Time:** XX ms

## 📖 References
- [Astra DB Documentation](https://www.datastax.com/products/datastax-astra)
- [MLflow Guide](https://mlflow.org/docs/latest/index.html)

