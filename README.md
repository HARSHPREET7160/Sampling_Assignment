# 📊 Sampling Techniques Comparison on Credit Card Fraud Dataset

## 📌 Project Overview
This project implements and compares **five different sampling techniques** on a **credit card fraud detection dataset** and evaluates their impact on the performance of **five machine learning models**.  
The primary goal is to analyze how different sampling strategies affect model accuracy after handling **class imbalance**.

---

## 1️⃣ Methodology

### 🔹 Sampling Techniques Used
- **Sample1 – Simple Random Sampling**  
  Random selection of observations from the balanced dataset.

- **Sample2 – Systematic Sampling**  
  Selection of every *k*th observation at regular intervals.

- **Sample3 – Stratified Sampling**  
  Proportional sampling that maintains the original class distribution.

- **Sample4 – Cluster Sampling**  
  Dataset divided into clusters, with random selection from chosen clusters.

- **Sample5 – Bootstrap Sampling**  
  Random sampling **with replacement**, allowing duplicate observations.

---

### 🔹 Machine Learning Models
- **M1:** Logistic Regression  
- **M2:** Decision Tree Classifier  
- **M3:** Random Forest Classifier  
- **M4:** Support Vector Machine (SVM)  
- **M5:** K-Nearest Neighbors (KNN)

---

## 2️⃣ Project Description

Credit card fraud datasets are typically **highly imbalanced**, making fraud detection challenging.  
This project addresses the issue through the following steps:

- Loaded a credit card transaction dataset with extreme imbalance  
  - **Legitimate transactions:** 763  
  - **Fraudulent transactions:** 9  
- Applied **Random Over-Sampling** to balance the dataset  
- Calculated optimal sample size using the statistical formula:

\[
n = \frac{Z^2 \times p \times (1 - p)}{E^2}
\]

- Final sample size used: **n = 384**
- Generated five samples using different sampling techniques
- Trained and evaluated five ML models on each sample
- Compared accuracy scores to identify optimal combinations

---

## 3️⃣ Input / Output

### 📥 Input
- **Dataset:** Credit card transaction data (CSV)
- **Features:** Anonymized transaction attributes
- **Target Variable:**  
  - `0` → Legitimate  
  - `1` → Fraudulent  

### 📤 Output
- Accuracy comparison table for all sampling–model combinations
- Best sampling technique for each model
- Best-performing model for each sampling technique
- Results file: **`sampling_results.csv`**

---

## 🔍 Key Findings

- **Random Forest (M3)** achieved **100% accuracy** on:
  - Sample1 (Simple Random)
  - Sample2 (Systematic)
  - Sample3 (Stratified)

- **Bootstrap Sampling (Sample5)** showed the **best overall performance**, achieving the highest average accuracy.

- All models demonstrated **significant performance improvement** after balancing the dataset.

---

## 4️⃣ Results Table

| Sampling Technique | M1 (LogReg) | M2 (Decision Tree) | M3 (Random Forest) | M4 (SVM) | M5 (KNN) |
|-------------------|------------|--------------------|--------------------|----------|----------|
| **Sample1** | 87.07% | 96.55% | **100.00%** | 87.07% | 90.52% |
| **Sample2** | 87.07% | 97.41% | **100.00%** | 85.34% | 95.69% |
| **Sample3** | 92.24% | **98.28%** | **100.00%** | 93.10% | 93.97% |
| **Sample4** | 92.24% | 96.55% | 98.28% | 94.83% | **96.55%** |
| **Sample5** | **98.28%** | 97.41% | 98.28% | **98.28%** | 96.55% |

---

## 🏆 Best Sampling–Model Combinations

- **Logistic Regression (M1)** → Sample5 (**98.28%**)  
- **Decision Tree (M2)** → Sample3 (**98.28%**)  
- **Random Forest (M3)** → Sample1 / Sample2 / Sample3 (**100.0%**)  
- **SVM (M4)** → Sample5 (**98.28%**)  
- **KNN (M5)** → Sample4 (**96.55%**)  

---

## 📌 Conclusion
The study highlights the critical role of **sampling techniques** in fraud detection tasks.  
While Random Forest consistently delivered superior performance, **Bootstrap Sampling** proved to be the most robust sampling strategy overall.

---

⭐ *If you find this project useful, consider giving it a star on GitHub!*
