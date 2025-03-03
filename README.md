# Gaussian Network Model (GNM) for Driver Activity Recognition

## Overview
This project implements a **Gaussian Network Model (GNM)** to recognize driver activities based on sensor data. The model leverages **Gaussian Mixture Models (GMM)** to probabilistically classify driving behaviors. The aim is to improve driver monitoring systems and enhance road safety through AI-driven behavioral analysis.

## Algorithm Explanation
### **Gaussian Network Model (GNM)**
The **GNM** is based on Gaussian Mixture Models (GMM), which use a probabilistic approach to classify data points into different clusters. Each cluster represents a different driver activity, and the model assigns probabilities to these activities based on input sensor data.

### **How It Works**
1. **Data Preprocessing:**  
   - The input data includes sensor readings such as acceleration, speed, and steering angles.
   - Features are standardized using **StandardScaler** to ensure optimal performance.
   - The target variable (driver activities) is **label-encoded** into numerical format.

2. **Model Training:**  
   - A **Gaussian Mixture Model (GMM)** is trained with a number of components equal to the unique activities.
   - The model uses **full covariance type** to capture interdependencies between features.
   - It learns the probability distribution of each activity from the training data.

3. **Prediction & Evaluation:**  
   - The trained model predicts the most probable activity class for new test data.
   - Performance is evaluated using **accuracy, precision, recall, and F1-score**.
   - The log-likelihood scores for training and test sets are also computed.

## Performance & Results
Due to the **limited dataset**, the model's performance is relatively low, as reflected in the accuracy and log-likelihood scores:
- **Train Accuracy:** 0.20
- **Test Accuracy:** 0.21
- **Overall Accuracy:** 0.21
- **Precision:** 0.20
- **Recall:** 0.21
- **F1-Score:** 0.20
- **Train Score:** -13.85
- **Test Score:** -14.36

### **Why Are the Scores Low?**
- The **dataset size is small**, limiting the model's ability to learn meaningful patterns.
- Gaussian models work best with **larger datasets** to accurately estimate distributions.
- Additional **feature engineering and data augmentation** could improve accuracy.

## How to Run the Code
### **Prerequisites**
Ensure you have the following installed:
- Python 3.x
- NumPy
- Scikit-learn

### **Steps to Run**
1. Clone the repository:
   ```bash
   git clone https://github.com/Mevin01/GNM.git
   ```
2. Navigate to the project folder:
   ```bash
   cd GNM
   ```
3. Run the script in a Python environment (or Jupyter Notebook):
   ```python
   python gnm_driver_activity.py
   ```

## Future Improvements
- **Increase dataset size** for better generalization.
- **Feature engineering** to improve representation.
- **Hybrid models** combining GMM with deep learning (e.g., LSTM + GMM).

Let's collaborate and improve **AI-driven driver activity recognition! 🚗💡**
