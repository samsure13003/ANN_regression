# ⚡ Power Plant Energy Output Prediction — Artificial Neural Network

A regression project using an Artificial Neural Network (ANN) built with TensorFlow/Keras to predict the **net hourly electrical energy output (PE)** of a combined cycle power plant based on four ambient sensor readings.

---

## 🛠️ Tech Stack

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange?logo=tensorflow)
![Keras](https://img.shields.io/badge/Keras-Sequential_API-red?logo=keras)
![Pandas](https://img.shields.io/badge/Pandas-Data_Handling-150458?logo=pandas)
![Scikit-learn](https://img.shields.io/badge/Scikit--Learn-Train_Test_Split-F7931E?logo=scikit-learn)

---

## 📌 Problem Statement

Combined cycle power plants combine gas and steam turbines to generate electricity. Their energy output fluctuates with ambient conditions. This project builds an ANN regression model that learns the relationship between environmental variables and power output, enabling more accurate energy planning and optimization.

---

## 📊 Dataset

**Source:** [UCI Machine Learning Repository — Combined Cycle Power Plant Dataset](https://archive.ics.uci.edu/ml/datasets/combined+cycle+power+plant)  
**File:** `Folds5x2_pp.xlsx`  
**Rows:** 9,568 hourly readings  
**Features:** 4 inputs, 1 output

| Feature | Description | Unit |
|--------|-------------|------|
| `AT` | Ambient Temperature | °C |
| `V` | Exhaust Vacuum | cm Hg |
| `AP` | Ambient Pressure | millibar |
| `RH` | Relative Humidity | % |
| `PE` | Net Electrical Energy Output *(target)* | MW |

### Feature Statistics

| | AT | V | AP | RH | PE |
|---|---|---|---|---|---|
| Mean | 19.65 | 54.31 | 1013.26 | 73.31 | 454.37 |
| Std | 7.45 | 12.71 | 5.94 | 14.60 | 17.07 |
| Min | 1.81 | 25.36 | 992.89 | 25.56 | 420.26 |
| Max | 37.11 | 81.56 | 1033.30 | 100.16 | 495.76 |

---

## 🧠 Model Architecture

```
Input Layer  →  4 features (AT, V, AP, RH)
Hidden Layer 1  →  6 neurons, ReLU activation
Hidden Layer 2  →  6 neurons, ReLU activation
Output Layer  →  1 neuron (linear, regression output)
```

Built with `tf.keras.models.Sequential` using the Keras functional API.

---

## ⚙️ Training Configuration

| Parameter | Value |
|-----------|-------|
| Optimizer | Adam |
| Loss Function | Mean Squared Error (MSE) |
| Batch Size | 32 |
| Epochs | 100 |
| Train/Test Split | 80% / 20% |

---

## 🗂️ Project Structure

```
📦 ann-power-plant/
├── Artificial_Neural_Network.ipynb   # Main notebook
├── Folds5x2_pp.xlsx                  # Dataset
└── README.md
```

---

## 🚀 Getting Started

### Prerequisites

```bash
pip install numpy pandas tensorflow scikit-learn openpyxl
```

### Run the Notebook

```bash
git clone https://github.com/your-username/ann-power-plant.git
cd ann-power-plant
jupyter notebook Artificial_Neural_Network.ipynb
```

---

---

## 👤 Author

**Samsur**  
Mechatronics Engineering Student — KUET  
[LinkedIn](https://linkedin.com/in/your-profile) · [GitHub](https://github.com/your-username)
