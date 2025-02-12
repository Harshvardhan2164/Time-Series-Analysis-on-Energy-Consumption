# Time-Series-Analysis-on-Energy-Consumption

## **Table of Contents**
- [Introduction](#introduction)
- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Model Architectures](#model-architectures)
  - [GRU Model](#gru-model)
  - [LSTM Model](#lstm-model)
- [Installation](#installation)
- [Usage](#usage)
- [Evaluation Metrics](#evaluation-metrics)
- [Results](#results)
- [Future Work](#future-work)
- [Contributors](#contributors)

---

## **Introduction**
DNA sequence prediction is a crucial task in bioinformatics, enabling researchers to analyze genetic patterns, predict mutations, and model gene structures. This project implements three machine learning approaches to predict nucleotide sequences: **N-Gram, LSTM, and Transformer models**.

## **Project Overview**
This project focuses on analyzing and predicting energy consumption using time series analysis techniques. It employs two deep learning models: Gated Recurrent Unit (GRU) and Long Short-Term Memory (LSTM), leveraging the moving average concept for trend analysis. The evaluation metric used for assessing model performance is Symmetric Mean Absolute Percentage Error (sMAPE).

By leveraging historical energy consumption data, the project aims to provide accurate forecasts that can be useful for:

- Optimizing energy distribution
- Detecting anomalies in power usage
- Improving energy efficiency strategies

## **Dataset**
We will be using the <a href="https://www.kaggle.com/datasets/robikscube/hourly-energy-consumption" target="_blank">PJM Interconnection LLC Energy Consumption Dataset</a> from Kaggle. This dataset provides hourly power consumption data for various regions across the United States.

Please download the dataset and place it in the `Dataset` directory.

## **Model Architectures**

### **N-Gram Model**
- A simpler alternative to LSTM with fewer parameters.
- Efficient in learning time-dependent patterns.
- Performs well with limited computational resources.

### **LSTM Model**
- Captures long-term dependencies in sequential data.
- Prevents vanishing gradient problem using gates.
- Suitable for learning energy consumption trends over time.

## **Installation**
To set up the project, follow these steps:

### **1. Clone the Repository**
```bash
git clone https://github.com/Harshvardhan2164/Time-Series-Analysis-on-Energy-Consumption.git
cd Time-Series-Analysis-on-Energy-Consumption
```

### **2. Setup a virtual enviorment**
```bash
python -m venv env
source env/Scripts/activate
```

### **3. Install Dependencies**
Ensure you have Python **3.8+** installed, then install required libraries:
```bash
pip install -r requirements.txt
```

## **Evaluation Metrics**
We use **sMAPE** to evaluate model performance:
- Unlike MAPE, it avoids division errors when actual values are close to zero.
- Provides a symmetric percentage error measurement.
- Ensures balanced performance assessment.

This is the formula for *sMAPE*:

$sMAPE = \frac{100}{n} \sum_{t=1}^n {2}\frac{|y_i - \hat{y}_i|}{|y_i| + |\hat{y}_i|}$

where:
- \( y_i \) = Actual value  
- \( \hat{y}_i \) = Predicted value  
- \( N \) = Number of data points

## **Result and Insights**
- The models effectively capture seasonal and trend patterns in energy consumption.
- GRU performs faster than LSTM due to fewer parameters, while LSTM shows better long-term dependency learning.
- sMAPE values indicate that the moving average preprocessing step improved forecasting accuracy.


## **Future Work**
- Implement hybrid models combining LSTM/GRU with Transformer architectures.
- Introduce external factors like weather conditions, industrial load, and economic activity.
- Deploy the trained model as an API for real-time energy forecasting.

## **Contributors**
- **Devansh Shrivastava** ([GitHub](https://github.com/devansh-srv))
- **Harshvardhan Sharma** ([GitHub](https://github.com/Harshvardhan2164))
- **Naman Jaswani** ([GitHub](https://github.com/Naman64000))
- **Vansh Jangir** ([GitHub](https://github.com/vanshjangir))
- **Vajrala Akhilesh** ([Github]())

---

### **License**
This project is licensed under the MIT License.