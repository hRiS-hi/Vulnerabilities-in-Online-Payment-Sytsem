# Online Payment Fraud Detection System

## Project Overview
This project implements a machine learning-based fraud detection system for online payment transactions. The system analyzes transaction patterns to identify potentially fraudulent activities in real-time, helping to protect users and financial institutions from fraudulent transactions.

## Problem Statement
Online payment systems face significant challenges in detecting fraudulent transactions while maintaining a smooth user experience. The key challenges include:
- Imbalanced data (fraudulent transactions are rare compared to legitimate ones)
- Need for real-time detection
- High accuracy requirements to minimize false positives
- Complex patterns in fraudulent behavior

## Dataset
- **Source**: Banksim Dataset
- **File**: fraud_detection_bankSim.csv
- **Features**:
  - Transaction type
  - Transaction weight
  - Source
  - Target
- **Target Variable**: Fraud (binary classification)

## Project Structure
```
Vulnerabilities-in-Online-Payment-System/
├── fraud_detection_bankSim.csv     # Dataset
├── fraudulent_payment_detection.ipynb  # Main analysis notebook
└── README.md                       # Project documentation
```

## Implementation Details

### Data Preprocessing
1. **Data Cleaning**:
   - Handling missing values
   - Removing duplicates
   - Data type conversion

2. **Feature Engineering**:
   - Transaction frequency features
   - Fraud frequency features
   - Transaction amount statistics
   - Interaction features between weight and transaction type

3. **Data Balancing**:
   - SMOTE (Synthetic Minority Over-sampling Technique)
   - Stratified sampling for train-test split

### Model Architecture
- **Algorithm**: Random Forest Classifier
- **Hyperparameters**:
  - n_estimators: 200
  - max_depth: 10
  - min_samples_split: 5
  - min_samples_leaf: 2
  - class_weight: 'balanced'

### Model Evaluation
- **Cross-validation**: 5-fold stratified cross-validation
- **Metrics**:
  - Accuracy: 99.2%
  - Precision (Fraud): 0.68
  - Recall (Fraud): 0.65
  - F1-score (Fraud): 0.67
  - AUC-ROC: 0.82

## Results and Analysis

### Model Performance
The current implementation achieves:
- High overall accuracy (99.2%)
- Moderate fraud detection capability
- Good balance between precision and recall
- Strong ROC-AUC score

### Key Findings
1. **Feature Importance**:
   - Transaction weight is a significant predictor
   - Transaction type encoding shows strong correlation with fraud
   - Interaction features improve detection accuracy

2. **Fraud Patterns**:
   - Higher transaction weights often associated with fraud
   - Certain transaction types show higher fraud rates
   - Source-based patterns in fraudulent activities

## Future Improvements
1. **Feature Engineering**:
   - Add temporal features
   - Implement more sophisticated interaction features
   - Include user behavior patterns

2. **Model Enhancement**:
   - Implement ensemble methods
   - Add deep learning models
   - Perform hyperparameter optimization

3. **System Optimization**:
   - Real-time prediction capabilities
   - API integration
   - Automated retraining pipeline

## Installation and Usage

### Prerequisites
- Python 3.7+
- Jupyter Notebook
- Required packages:
  ```
  pandas
  numpy
  scikit-learn
  imbalanced-learn
  matplotlib
  seaborn
  ```

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/Vulnerabilities-in-Online-Payment-System.git
   ```

2. Install required packages:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the Jupyter notebook:
   ```bash
   jupyter notebook fraudulent_payment_detection.ipynb
   ```

## Project Workflow
1. **Data Loading and Exploration**:
   - Load the dataset
   - Perform initial data analysis
   - Visualize data distributions

2. **Data Preprocessing**:
   - Clean and preprocess the data
   - Handle missing values
   - Encode categorical variables

3. **Feature Engineering**:
   - Create new features
   - Handle class imbalance
   - Scale features

4. **Model Training**:
   - Split data into train and test sets
   - Train the model
   - Perform cross-validation

5. **Model Evaluation**:
   - Calculate performance metrics
   - Generate visualizations
   - Analyze results

## Contributing
Contributions are welcome! Please feel free to submit a Pull Request.

## License
This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments
- Banksim Dataset providers
- Scikit-learn and imbalanced-learn communities
- Contributors and maintainers of the project