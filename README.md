# π©Ί Diabetes Prediction Model β Your First MLOps Project (FastAPI + Docker + K8s)

> π₯ YouTube video for the project: **"Build Your First MLOps Project"**

This project helps you learn **Building and Deploying an ML Model** using a simple and real-world use case: predicting whether a person is diabetic based on health metrics. Weβll go from:

- β Model Training
- β Building the Model locally
- β API Deployment with FastAPI
- β Dockerization
- β Kubernetes Deployment

---

## π Problem Statement

Predict if a person is diabetic based on:
- Pregnancies
- Glucose
- Blood Pressure
- BMI
- Age

We use a Random Forest Classifier trained on the **Pima Indians Diabetes Dataset**.

---

## π Quick Start

### 1. Clone the Repo

```bash
git clone https://github.com/iam-veeramalla/first-mlops-project.git
cd first-mlops-project
```

### 2. Create Virtual Environment

```
python3 -m venv .mlops
source .mlops/bin/activate
```

### 3. Install Dependencies

```
pip install -r requirements.txt
```

## Train the Model

```
python train.py
```

## Run the API Locally

```
uvicorn main:app --reload
```

### Sample Input for /predict

```
{
  "Pregnancies": 2,
  "Glucose": 130,
  "BloodPressure": 70,
  "BMI": 28.5,
  "Age": 45
}
```

## Dockerize the API

### Build the Docker Image

```
docker build -t diabetes-prediction-model .
```

### Run the Container

```
docker run -p 8000:8000 diabetes-prediction-model
```

## Deploy to Kubernetes

```
kubectl apply -f diabetes-prediction-model-deployment.yaml
```

π Credits

Created by `ABHISHEK VEERAMALLA`

Subscribe for more DevOps + MLOps content on the YouTube Channel - `Abhishek.Veeramalla`

Trigger CI/CD νΊ
test trigger
