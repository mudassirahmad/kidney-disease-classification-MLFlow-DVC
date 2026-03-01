# Kidney Disease Classification (MLflow + DVC)

This project is an end-to-end deep learning pipeline for classifying kidney diseases from CT scan images. It demonstrates how to build a reproducible ML system using **transfer learning**, **MLflow experiment tracking**, and **DVC pipelines**.

This project is built with MLOps-style deep learning workflow.

---

## Project Overview

This project:

- Uses **VGG16 transfer learning**
- Builds a modular training pipeline  
- Tracks experiments with **MLflow**
- Versions data and pipelines with **DVC**
- Provides a simple prediction app

---

## 🧩 Workflow

The end-to-end pipeline includes:

1. Data Ingestion  
2. Prepare Base Model  
3. Model Training  
4. Model Evaluation  
5. Prediction Pipeline  
6. Experiment Tracking (MLflow)  
7. Pipeline Orchestration (DVC)

---

## Project Structure

├── config/ # Configuration files

├── src/ # Source code (pipeline components)

├── research/ # Experiment notebooks

├── artifacts/ # Generated outputs

├── dvc.yaml # DVC pipeline definition

├── params.yaml # Hyperparameters

├── app.py # Flask prediction app

├── main.py # Training pipeline entry point

└── requirements.txt # Dependencies


---

## Tech Stack

- Python  
- Keras  
- VGG16 (Transfer Learning)  
- MLflow  
- DVC  
- Flask  
- Docker

---

## How to Run the Project

### Step 1 — Clone the repo

```bash
git clone https://github.com/mudassirahmad/kidney-disease-classification-MLFlow-DVC
cd kidney-disease-classification-MLFlow-DVC
```


### Step 2 — Create Environment

Create a new Conda environment and activate it:

```bash
conda create -n kidney python=3.8 -y
conda activate kidney
```

### Step 3 — Install Dependencies

Install all required Python packages:
```bash
pip install -r requirements.txt
```
Step 4 — Run Training Pipeline

### Run the training script:
```bash
python main.py
```
OR run the pipeline using DVC:
```bash
dvc repro
```
### Step 5 — Run the App

If running locally:
```bash
python app.py
```
Or access the live app directly on the EC2 instance:

[Open Live App on EC2](http://15.135.164.86:8080/)


## Model Details

- Base Model: VGG16 (ImageNet weights)
- Approach: Transfer Learning
- Custom fully connected layers added
- Image classification from CT scans

