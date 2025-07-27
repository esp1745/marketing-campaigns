# Customer Campaign Response Prediction

## Overview

This project builds a machine learning model to predict customer responses to marketing campaigns using historical interaction data. The goal is to identify high-potential customers and improve targeting efficiency through data-driven decisions.

## Dataset

- Source: `hist.csv`  
- Size: ~260,000 rows  
- Features:
  - week_id
  - customer_id
  - attribute1
  - state_id
  - Sex
  - campaign_id
  - response (target: 0 = No, 1 = Yes)

## Project Setup

### Requirements

Make sure you have Python 3.8 or higher installed. Then install the required packages using:

```bash
pip install -r requirements.txt
```

### Key Dependencies

- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- jupyter

### How to Run

1. Clone the repository or download the files.
2. Place `hist.csv` in the root directory.
3. Launch the notebook:

```bash
jupyter notebook demo.ipynb
```

4. Run all cells to preprocess data, train the model, evaluate results, and generate visualizations.

## Exploratory Data Analysis (EDA)

- Visualized the response distribution and correlation matrix
- Identified class imbalance (more 0s than 1s)
- Weak to moderate correlation observed between some features and the target

## Model Building

- Model Used: Random Forest Classifier
- Tools: scikit-learn, pandas, matplotlib, seaborn
- Model trained on 80% of the data and tested on 20%
- Evaluation metrics: accuracy, precision, recall, F1-score
- Top important features:
  - campaign_frequency
  - state_id
  - prior_responses
  - attribute1
  - campaigns_seen

## Key Results

- Top 25% of customers most likely to respond:
  ```
  [5819, 3649, 7769, 5869, 5496, 9126, 12596, 21, 8632, 2749]
  ```

- Expected Response Rate for Week 27:
  ```
  74.19%
  ```

## Deliverables

- `Customer_Response_Report.docx`: Full detailed analysis report

## Future Enhancements

- Experiment with XGBoost, LightGBM, or logistic regression for improved performance
- Address class imbalance with SMOTE or class weights
- Integrate prediction outputs with marketing automation tools
- Automate weekly response forecasting and reporting

## Author
Esparance Tuyishime
esparance7@gmail.com 
