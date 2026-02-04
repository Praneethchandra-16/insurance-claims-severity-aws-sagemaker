# Insurance Claims Severity Prediction with AWS SageMaker

## Overview
This project implements an end-to-end machine learning workflow to predict insurance claim severity using supervised regression techniques. The objective is to estimate claim severity in advance to support risk assessment, cost forecasting, and decision support in insurance and financial services contexts.

The project focuses not only on model training, but also on reproducible data handling, cloud-based model deployment, and production-style inference workflows using AWS services.

## Problem Statement
Insurance providers and financial institutions must assess the potential severity of claims early in the lifecycle to optimize claims handling, prioritize investigations, and manage financial exposure. This project frames claim severity estimation as a regression problem using historical claims data and demonstrates how such a model can be trained, evaluated, and deployed using AWS-native tooling.

## Dataset
The model was trained on an insurance claims dataset containing structured policy, customer, and claim attributes.

Due to size and sensitivity considerations, the full dataset is not committed to this repository. A representative sample dataset is included to demonstrate data structure and enable reproducibility.

Users can replace the sample dataset with the full dataset locally by following the instructions in the training notebook.

## Modeling Approach
- Supervised regression formulation for claim severity prediction
- Feature engineering on structured tabular data
- Gradient-boosted decision tree modeling using XGBoost
- Iterative experimentation and validation
- Performance evaluation using RMSE, MAE, and error distribution analysis

## Cloud Architecture
The project follows a production-oriented AWS architecture:

- Amazon S3 for dataset storage and model artifact versioning
- AWS SageMaker for model training and endpoint configuration
- AWS Lambda for serverless inference
- Custom Lambda layers to manage ML dependencies such as XGBoost, Pandas, and Joblib

This separation of training, packaging, and inference reflects real-world ML deployment patterns used in enterprise environments.

## Repository Structure
<img width="672" height="678" alt="image" src="https://github.com/user-attachments/assets/c55909ff-12cd-4cf9-8826-b81fa334954f" />

## Notebooks
- `01_train_claim_severity_xgboost.ipynb`  
  Covers data loading, feature engineering, model training, evaluation, and artifact persistence.

- `02_deploy_sagemaker_endpoint.ipynb`  
  Demonstrates model packaging, S3 artifact management, and SageMaker endpoint configuration.

## Deployment Notes
Endpoints created during development were tested and later removed to avoid ongoing infrastructure costs. The repository focuses on demonstrating the full deployment workflow, configuration patterns, and production considerations rather than maintaining a continuously running endpoint.

## How to Run Locally
1. Clone the repository
2. Create a Python environment with required dependencies
3. Run the training notebook using the sample dataset
4. Review deployment notebook for SageMaker configuration and endpoint creation steps
5. Use the provided sample payload to test inference logic

## Key Takeaways
- Demonstrates end-to-end ownership of a machine learning workflow
- Shows practical experience with AWS SageMaker and serverless inference
- Emphasizes reproducibility, scalability, and production readiness
- Aligns modeling decisions with business interpretability and risk considerations

## Author
Praneeth Chandra Budala  
Dallas, Texas, USA

LinkedIn  
https://www.linkedin.com/in/praneeth-chandra-budala-6795b8214/ 

Portfolio  
https://praneeths-ai-career.lovable.app

GitHub  
https://github.com/Praneethchandra-16

## Disclaimer
This project is for educational and demonstration purposes. It does not represent production systems or proprietary data from any organization.
