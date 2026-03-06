# Predictive-Maintenance-of-smart-manufacturing-Energy-Turbines

---

# Predictive Maintenance using CNN-LSTM

### Remaining Useful Life (RUL) Prediction for Industrial Machines

![Python](https://img.shields.io/badge/Python-3.10-blue)
![TensorFlow](https://img.shields.io/badge/TensorFlow-Deep%20Learning-orange)
![License](https://img.shields.io/badge/License-Academic-green)
![Status](https://img.shields.io/badge/Status-Research%20Project-success)

---

# Project Overview

This project implements a **Predictive Maintenance System** that estimates the **Remaining Useful Life (RUL)** of industrial machines using IoT sensor data. The system processes high-dimensional sensor datasets and applies a **CNN-LSTM hybrid deep learning model** to capture both spatial patterns and time-series dependencies.

By predicting machine degradation early, the system helps industries **reduce downtime, optimize maintenance schedules, and improve operational efficiency**.

---

# Problem Statement

Industrial equipment often fails unexpectedly, leading to production delays and increased maintenance costs. Traditional maintenance methods rely on fixed schedules or manual inspection and cannot accurately predict machine failures.

This project uses machine learning and deep learning techniques to analyze IoT sensor data and predict the **Remaining Useful Life (RUL)** of machines, enabling proactive maintenance.

---

# Dataset

Dataset used:

```
RealTime_IoT_PredictiveMaintenance_Dataset.csv
```

Dataset statistics:

| Attribute            | Value        |
| -------------------- | ------------ |
| Initial dataset size | 177,763 × 91 |
| After preprocessing  | 177,763 × 87 |
| Feature matrix       | 177,763 × 86 |

The dataset contains machine sensor data such as operational parameters and timestamps used to compute RUL. 

---

# Project Workflow

```
IoT Sensor Data
       │
       ▼
Data Loading
       │
       ▼
Data Cleaning & Outlier Handling
       │
       ▼
Feature Encoding & Normalization
       │
       ▼
Sequence Generation (Time-Series)
       │
       ▼
Train-Test Split
       │
       ▼
CNN-LSTM Model Training
       │
       ▼
Model Evaluation & Visualization
       │
       ▼
RUL Prediction
```

---

# Model Architecture

The predictive model combines **Convolutional Neural Networks (CNN)** and **Long Short-Term Memory (LSTM)** networks.

### CNN-LSTM Layers

1. Conv1D (Feature extraction from sensor signals)
2. Batch Normalization
3. MaxPooling1D
4. Dropout (Regularization)
5. LSTM Layer (Temporal pattern learning)
6. Dense Layers (Regression output)

Total Parameters: **51,969**

Loss Function

```
Mean Squared Error (MSE)
```

Evaluation Metric

```
Mean Absolute Error (MAE)
```

---

# Model Training

Training configuration:

| Parameter        | Value |
| ---------------- | ----- |
| Epochs           | 5     |
| Batch Size       | 32    |
| Validation Split | 20%   |
| Optimizer        | Adam  |

Callbacks used:

* EarlyStopping
* ReduceLROnPlateau

These help improve training stability and prevent overfitting. 

---

# Model Performance

| Metric                  | Value      |
| ----------------------- | ---------- |
| RUL Prediction Accuracy | **84.27%** |
| Model Accuracy          | **90.03%** |
| RUL Prediction Error    | **15.73%** |

Example output:

```
Actual RUL (%): 16.79
RUL Prediction Accuracy (%): 84.27
Model Accuracy (%): 90.03
```

---

# Visualization

The training process includes **loss curves** to monitor model convergence.

Graphs show:

* Training loss
* Validation loss

These visualizations help analyze model performance during training.

---

# Technology Stack

### Programming Language

* Python

### Libraries

* Pandas
* NumPy
* Scikit-learn
* TensorFlow / Keras
* Matplotlib
* Seaborn

### Machine Learning

* CNN-LSTM Deep Learning Model

---

# Project Structure

```
Predictive-Maintenance-CNN-LSTM
│
├── dataset
│   └── RealTime_IoT_PredictiveMaintenance_Dataset.csv
│
├── notebooks
│   └── PDM_SEM8.ipynb
│
├── src
│   ├── preprocessing.py
│   ├── sequence_generation.py
│   ├── model_training.py
│   └── evaluation.py
│
├── results
│   └── loss_plot.png
│
└── README.md
```

---

# Installation

### 1. Clone Repository

```
git clone https://github.com/yourusername/predictive-maintenance-cnnlstm.git
```

### 2. Navigate to Project

```
cd predictive-maintenance-cnnlstm
```

### 3. Install Dependencies

```
pip install pandas numpy scikit-learn tensorflow matplotlib seaborn
```

---

# Usage

Run the notebook or script to train the model.

Example:

```
python model_training.py
```

or run the **Google Colab Notebook**.

---

# Key Features

* Remaining Useful Life (RUL) prediction
* Large-scale IoT sensor dataset processing
* Time-series sequence generation
* CNN-LSTM hybrid architecture
* Automated preprocessing pipeline
* Performance evaluation with visualisation

---

# Future Improvements

* Real-time IoT data streaming
* Model deployment using cloud platforms
* Hyperparameter tuning for improved accuracy
* Integration with industrial dashboards
* Automated maintenance alert system

---

# Authors

Tammineni Rohit Kumar Reddy, 
Ganginepalli Sai Poojitha Raj, 
Reena B, 
Thota Joshitha, 

Supervisor
Dr. Ummadi Janardhan Reddy

---

# License

This project is developed for **academic and research purposes**.
