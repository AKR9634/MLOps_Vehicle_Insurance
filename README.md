# 🚗 Vehicle Insurance MLOps Project

### End-to-End Production-Grade Machine Learning Pipeline on AWS

![Python](https://img.shields.io/badge/Python-3.10-blue)
![AWS](https://img.shields.io/badge/AWS-EC2%20%7C%20S3%20%7C%20ECR-orange)
![Docker](https://img.shields.io/badge/Docker-Containerized-blue)
![MongoDB](https://img.shields.io/badge/MongoDB-Atlas-green)
![CI/CD](https://img.shields.io/badge/CI%2FCD-GitHub_Actions-success)
![Status](https://img.shields.io/badge/Project-Production_Ready-brightgreen)

> A **real-world MLOps project** demonstrating how to build, train, validate, deploy, and continuously deliver machine learning models using **industry best practices**.

---

## 🔥 Why This Project Matters

Recruiters don’t just want models — they want **deployable, scalable, automated ML systems**.

This project showcases:

* ✅ Complete **MLOps lifecycle**
* ✅ **Cloud-native deployment (AWS)**
* ✅ **CI/CD automation**
* ✅ **Model versioning & evaluation**
* ✅ **Production-ready code structure**

---

## 🧠 What This Project Does

* Predicts **Vehicle Insurance outcomes**
* Uses **MongoDB Atlas** for scalable data storage
* Trains & validates ML models with strict schema checks
* Automatically evaluates and versions models
* Deploys via **Docker + AWS EC2**
* CI/CD pipeline triggered on every GitHub push

---

## 🏗️ System Architecture (High Level)

```
Data Source
   ↓
MongoDB Atlas
   ↓
Data Ingestion
   ↓
Data Validation
   ↓
Data Transformation
   ↓
Model Training
   ↓
Model Evaluation
   ↓
AWS S3 (Model Registry)
   ↓
Dockerized Flask App
   ↓
AWS EC2 (Production)
```

---

## 🗂️ Project Structure (Clean & Modular)

```
├── src/
│   ├── components/        # Core ML pipeline stages
│   ├── configuration/    # MongoDB & AWS configs
│   ├── constants/        # Centralized constants
│   ├── entity/           # Config & artifact entities
│   ├── data_access/      # DB interaction layer
│   ├── aws_storage/      # S3 model registry logic
│   ├── utils/            # Reusable utilities
│
├── notebook/             # EDA & Feature Engineering
├── .github/workflows/    # CI/CD pipeline
├── Dockerfile
├── app.py                # Prediction API
├── requirements.txt
└── README.md
```

---

## ⚙️ Local Setup (Developer Friendly)

```bash
conda create -n vehicle_insurance python=3.10 -y
conda activate vehicle_insurance
pip install -r requirements.txt
```

Verify:

```bash
pip list
```

---

## 🗄️ MongoDB Atlas Integration

* Cloud-based **NoSQL database**
* Secure connection via **environment variables**
* Data pushed directly from Jupyter notebooks
* Schema-validated before training

```bash
export MONGODB_URL="mongodb+srv://<username>:<password>@cluster.mongodb.net/"
```

---

## 🧾 Logging & Exception Handling

✔ Centralized logging
✔ Custom exception classes
✔ Debug-friendly stack traces
✔ Tested via demo scripts

---

## 📥 Data Ingestion Pipeline

* Reads data from MongoDB
* Converts JSON → DataFrame
* Stores artifacts for downstream stages
* Fully configurable & reusable

---

## ✅ Data Validation

* Schema defined in `schema.yaml`
* Validates:

  * Column names
  * Data types
  * Missing values
* Prevents **silent data drift**

---

## 🔄 Data Transformation

* Feature engineering
* Encoding & scaling
* Train/test split
* Reusable transformation pipeline

---

## 🤖 Model Training

* Modular estimator design
* Hyperparameter-ready
* Clean separation of concerns
* Artifacts tracked after training

---

## 🔍 Model Evaluation & Registry (AWS S3)

* Compares **new vs production model**
* Threshold-based promotion:

  ```python
  MODEL_EVALUATION_CHANGED_THRESHOLD_SCORE = 0.02
  ```
* Best model stored in **S3 model registry**

---

## ☁️ AWS Stack Used

| Service        | Purpose              |
| -------------- | -------------------- |
| EC2            | Model hosting        |
| S3             | Model registry       |
| ECR            | Docker image storage |
| IAM            | Secure access        |
| GitHub Actions | CI/CD                |

---

## 🚀 CI/CD Pipeline (Fully Automated)

**On every push:**

1. GitHub Actions triggered
2. Docker image built
3. Image pushed to AWS ECR
4. Deployed on EC2 via self-hosted runner
5. App goes live 🚀

---

## 🌐 Live Application

```text
http://<EC2-PUBLIC-IP>:5000
```

Endpoints:

* `/predict` → Get predictions
* `/training` → Trigger training pipeline

---

## 🐳 Dockerized Deployment

```bash
docker build -t vehicle-insurance .
docker run -p 5000:5000 vehicle-insurance
```

---

## 🧩 Tech Stack

* **Python 3.10**
* **Scikit-learn, Pandas, NumPy**
* **MongoDB Atlas**
* **AWS (EC2, S3, ECR, IAM)**
* **Docker**
* **GitHub Actions**
* **Flask**

---

## 🧑‍💼 Ideal For Recruiters Looking For

✔ MLOps Engineer
✔ ML Engineer
✔ Data Scientist (Production ML)
✔ Cloud + ML skillset

---

## 👤 Author

**Akhil**
: Aspiring **MLOps / Machine Learning Engineer**
Focused on building **scalable, production ML systems**

📫 *Open to internships & full-time roles*

---

## ⭐ If You Like This Project

* Give it a ⭐
* Fork it 🍴
* Use it as an MLOps reference 📘

