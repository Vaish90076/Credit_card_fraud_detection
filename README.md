# 🚀 AI-Driven Real-Time Fraud Detection System

An end-to-end **Big Data and Machine Learning pipeline** for detecting fraudulent financial transactions in real time. The system leverages **Apache Kafka**, **Apache Spark Streaming**, **XGBoost**, **FastAPI**, and **Streamlit** to process live transaction streams, predict fraud, store results, and visualize insights through an interactive dashboard.

---

## 📌 Project Overview

Financial institutions process millions of transactions daily, making real-time fraud detection critical for minimizing financial losses and improving security.

This project simulates a production-grade fraud detection workflow where transaction events are streamed through Kafka, processed by Spark Streaming, analyzed using a machine learning model, and displayed on a live dashboard.

---

## 🏗️ System Architecture

```text
Transaction Generator
        │
        ▼
   Apache Kafka
        │
        ▼
Apache Spark Streaming
        │
        ▼
 Feature Engineering
        │
        ▼
 XGBoost ML Model
        │
        ▼
 PostgreSQL / SQLite
        │
        ├──► FastAPI
        │
        ▼
 Streamlit Dashboard
```

---

## ✨ Key Features

* Real-time transaction streaming
* Distributed stream processing with Apache Spark
* Machine learning–based fraud prediction
* Automated feature engineering pipeline
* Historical transaction storage
* Interactive analytics dashboard
* REST API for fraud insights
* Scalable architecture for high-volume transaction processing

---

## 🛠️ Technology Stack

| Category         | Technologies           |
| ---------------- | ---------------------- |
| Programming      | Python                 |
| Streaming        | Apache Kafka           |
| Processing       | Apache Spark (PySpark) |
| Machine Learning | Scikit-Learn, XGBoost  |
| Database         | PostgreSQL / SQLite    |
| API Development  | FastAPI                |
| Dashboard        | Streamlit              |
| Data Processing  | Pandas, NumPy          |

---

## 📂 Project Structure

```text
fraud-detection-system/
│
├── data/
├── kafka/
├── spark/
├── ml_model/
├── database/
├── api/
├── dashboard/
├── utils/
├── requirements.txt
└── README.md
```

---

## ⚙️ Installation

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/fraud-detection-system.git
cd fraud-detection-system
```

### 2. Create a Virtual Environment

```bash
python -m venv venv
```

Activate the environment:

**Windows**

```bash
venv\Scripts\activate
```

**Linux/macOS**

```bash
source venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

---

## 🔧 Setup Instructions

### Start Apache Kafka

Start Zookeeper:

```bash
bin/zookeeper-server-start.sh config/zookeeper.properties
```

Start Kafka Server:

```bash
bin/kafka-server-start.sh config/server.properties
```

Create Kafka Topics:

```bash
bin/kafka-topics.sh --create --topic transactions --bootstrap-server localhost:9092

bin/kafka-topics.sh --create --topic fraud_predictions --bootstrap-server localhost:9092
```

---

### Configure Database

```bash
python database/db_setup.py
```

---

### Train the Fraud Detection Model

```bash
python ml_model/train_model.py
```

This generates the trained model file:

```text
fraud_model.pkl
```

---

## ▶️ Running the Project

### Start Spark Streaming Processor

```bash
python spark/spark_stream_processor.py
```

### Start Transaction Producer

```bash
python kafka/producer.py
```

### Launch Dashboard

```bash
streamlit run dashboard/dashboard.py
```

### Launch FastAPI Server (Optional)

```bash
uvicorn api.app:app --reload
```

---

## 🔄 Workflow

1. Transaction data is generated continuously.
2. Kafka streams transaction events in real time.
3. Spark Streaming consumes and processes the data.
4. Feature engineering extracts relevant fraud indicators.
5. XGBoost predicts fraud probability.
6. Predictions are stored in the database.
7. Streamlit dashboard displays real-time analytics.
8. FastAPI exposes prediction data through REST endpoints.

---

## 📊 Dashboard Insights

The dashboard provides:

* Total Transactions Processed
* Fraudulent Transaction Count
* Fraud Rate Analysis
* Live Transaction Feed
* Fraud Trends Over Time
* Transaction Volume Monitoring
* Prediction Distribution Analytics

---

## 🤖 Machine Learning Pipeline

### Feature Engineering

* Transaction amount analysis
* Time-based features
* Frequency-based patterns
* Behavioral indicators

### Model

* XGBoost Classifier
* Scikit-Learn Preprocessing Pipeline

### Outputs

* Fraud Probability Score
* Fraud Classification
* Prediction Confidence

---

## 🎯 Learning Outcomes

This project demonstrates practical experience with:

* Real-Time Data Streaming
* Big Data Processing
* Data Engineering Pipelines
* Machine Learning Deployment
* Fraud Analytics
* API Development
* Dashboard Development
* End-to-End System Integration

---

## 💼 Relevant Roles

This project aligns with:

* Data Engineer
* Big Data Engineer
* Data Scientist
* Machine Learning Engineer
* Analytics Engineer
* AI Engineer
* Backend Engineer
* MLOps Engineer

---

## 🔮 Future Enhancements

* Docker Containerization
* Kubernetes Deployment
* Cloud Integration (AWS/Azure/GCP)
* Real-Time Alerting System
* Model Monitoring & Retraining
* Advanced Deep Learning Models
* CI/CD Pipeline Integration

---

## ⭐ If you found this project useful, consider giving it a star!
