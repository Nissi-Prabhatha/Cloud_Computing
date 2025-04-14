# 🍷 Wine Quality Prediction using PySpark on AWS EMR

## 📝 Project Overview

This project focuses on predicting the quality of wine based on its physicochemical properties using machine learning. The model is developed using **PySpark** and is trained on a distributed computing environment using **AWS EMR (Elastic MapReduce)**, which enables faster processing of large datasets.

After training, the model is stored in **Amazon S3** for reuse. A separate module allows predictions on new test data with performance evaluated using the **F1 score**. To support easy deployment, the entire pipeline is also containerized using **Docker**, allowing the model to be executed locally without the need for setting up an EMR cluster.

This project demonstrates real-world application of **cloud-based machine learning**, **big data processing**, and **containerization**, reflecting both system design and software engineering skills.

---

## 📌 Objective

To train and evaluate a wine quality prediction model using distributed computing on Amazon EMR, store the model in S3, and optionally run it locally via a Docker container with minimal setup.

---

## 📊 Dataset

- Source: UCI Machine Learning Repository  
- Training File: `TrainingDataset.csv`  
- Validation File: `ValidationDataset.csv`  
- Features: Physicochemical properties (e.g., acidity, alcohol, pH)  
- Target: Wine quality score (0–10)

---

## ⚙️ Technologies & Tools

| Technology    | Purpose                            |
|---------------|-------------------------------------|
| **Python 3**  | Core programming language           |
| **PySpark**   | Distributed data processing & ML    |
| **AWS EMR**   | Scalable Hadoop/Spark environment   |
| **Amazon S3** | Data storage and model persistence  |
| **Docker**    | Containerizing the trained model    |

---

## 📁 Project Structure

```bash
.
├── winequalityprediction.py           # Spark-based ML model training script
├── winequalitytestdataprediction.py   # Model loading and prediction with F1 score
├── Dockerfile                         # Docker config to build container image
├── TrainingDataset.csv                # Training dataset (uploaded to S3)
├── ValidationDataset.csv              # Test/validation dataset
