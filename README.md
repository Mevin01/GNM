# Driver Activity Recognition using Fuzzy Rule-Based Network and Gaussian Models

## Overview
This project implements **Driver Activity Recognition** using a **Fuzzy Rule-Based Network**, **Gaussian Mixture Model (GMM)**, and **Gaussian Network Model (GNM)**. These models analyze driver activities based on extracted features from the **StateFarm Distracted Driver Dataset** to assess driver alertness and identify risky behaviors.

## Algorithm Explanation
### **Fuzzy Rule-Based Network**
A **Fuzzy Rule-Based Network** leverages fuzzy logic principles to map driver activity levels to alertness scores using predefined membership functions and rules.

#### **Working Mechanism:**
1. **Fuzzy Variables:**
   - **Activity** (Input): Represents driver actions with values ranging from 0 to 10.
   - **Alertness** (Output): Indicates the driver's level of attention.
   
2. **Membership Functions:**
   - **Activity & Alertness** are categorized into three levels: **Poor, Average, and Good**.

3. **Fuzzy Rules:**
   - If **Activity is Poor**, then **Alertness is Poor**.
   - If **Activity is Average**, then **Alertness is Average**.
   - If **Activity is Good**, then **Alertness is Good**.

4. **Inference and Decision Making:**
   - The fuzzy system processes each driver's activity level and assigns an alertness score.
   - The final alertness score is mapped to a discrete class for classification.

### **Gaussian Mixture Model (GMM) and Gaussian Network Model (GNM)**
Both **GMM** and **GNM** use probabilistic clustering techniques to classify driver activities.

#### **Working Mechanism:**
1. **Data Preprocessing:**
   - Features are standardized to ensure a uniform distribution.
   - Labels are encoded for classification.
   
2. **Model Training:**
   - **GMM** uses unsupervised learning to find the probability distribution of different driver activity states.
   - **GNM** extends GMM by modeling full covariance between feature distributions.
   
3. **Prediction:**
   - The trained models predict the most likely driver activity class.
   
## Dataset
- **Training Set:** Preprocessed driver activity features extracted from the dataset.
- **Test Set:** Unseen driver activity data for performance evaluation.

## Implementation Steps
1. **Load and preprocess the dataset.**
2. **Define fuzzy variables and membership functions (for fuzzy logic).**
3. **Train GMM and GNM models on standardized features.**
4. **Apply fuzzy rules and Gaussian models for classification.**
5. **Evaluate model performance using accuracy, precision, recall, and F1-score.**

## Performance Metrics
Due to dataset constraints, the models’ performance is currently limited:

### **Fuzzy Rule-Based Network:**
- **Train Accuracy:** 21%
- **Test Accuracy:** 20%
- **Overall Accuracy:** 20%
- **Precision:** 49%
- **Recall:** 20%
- **F1-Score:** 11%

### **Gaussian Mixture Model (GMM) & Gaussian Network Model (GNM):**
- **Train Accuracy:** 20%
- **Test Accuracy:** 21%
- **Overall Accuracy:** 21%
- **Precision:** 20%
- **Recall:** 21%
- **F1-Score:** 20%
- **Train Score:** -13.85 (GNM)
- **Test Score:** -14.36 (GNM)

### **Why is Accuracy Low?**
1. **Simplified Rules:** A more complex rule set may improve classification.
2. **Limited Feature Representation:** The models rely on an aggregated activity measure.
3. **Dataset Size:** Increasing the dataset would enhance learning.

## How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/driver-activity-recognition.git
   cd driver-activity-recognition
   ```
2. Install dependencies:
   ```bash
   pip install numpy scikit-learn scikit-fuzzy
   ```
3. Run the script in **Google Colab** or locally:
   ```bash
   python driver_activity_recognition.py
   ```

## Future Improvements
- Implement **more granular fuzzy membership functions**.
- Optimize **fuzzy rule definitions** for better classification.
- Improve **Gaussian model feature selection** for better clustering.
- Explore **hybrid models combining fuzzy logic with machine learning**.
- Expand the dataset for improved accuracy.

