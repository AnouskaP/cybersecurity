# Cyber Attack Detection and Classification

## Project Overview
This project aims to analyze and classify different types of cyber attacks using **machine learning techniques**. The dataset includes various types of network intrusions, and the objective is to build predictive models that can effectively detect and classify attacks.

## Dataset
- The dataset consists of network traffic data categorized into different attack types.
- Attack categories include **Denial of Service (DoS), Probe, Remote-to-Local (R2L), and User-to-Root (U2R)**.
- Each record contains multiple network features along with a label indicating attack type or normal traffic.

## Project Workflow
1. **Data Preprocessing**
   - Load multiple CSV files and merge them into a single dataset.
   - Assign attack labels to each dataset.
   - Handle missing values and drop irrelevant/skewed features.
   
2. **Feature Engineering**
   - Convert categorical variables to numerical using one-hot encoding.
   - Remove outliers using **quantile-based capping**.
   - Compute **Weight of Evidence (WOE)** and **Information Value (IV)** for feature selection.
   
3. **Feature Selection**
   - Use **Univariate Selection, Recursive Feature Elimination (RFE), and SelectKBest** to identify the most relevant features.
   - Compute **Variance Inflation Factor (VIF)** to eliminate multicollinearity.
   
4. **Model Training and Evaluation**
   - Implement **Logistic Regression, Random Forest Classifier**, and other models.
   - Perform **ROC-AUC analysis** and compute **Gini Index**.
   - Optimize decision thresholds using **ROC curve**.
   
5. **Multi-class Classification**
   - Convert binary classification model into a multi-class model.
   - Train using **Random Forest and Logistic Regression**.
   - Evaluate using **precision, recall, and F1-score**.
   
## Installation & Dependencies
To run this project, install the required Python libraries:

```bash
pip install numpy pandas matplotlib seaborn statsmodels scikit-learn
```

## Usage
Clone the repository and run the script:

```bash
git clone https://github.com/your-username/cyber-attack-detection.git
cd cyber-attack-detection
python main.py
```

## Results & Findings
- The best model achieved high accuracy in detecting and classifying different types of cyber attacks.
- **ROC-AUC and Gini Index** were used to evaluate model performance.
- The **Random Forest model** outperformed other models in multi-class classification.

## Future Work
- Experiment with **Deep Learning models (LSTMs, CNNs)** for better feature extraction.
- Apply **Anomaly Detection techniques** for zero-day attacks.
