Iterative LLM-Guided Feature Extraction for Clinical Trial Outcome Prediction
Overview
This repository implements a feedback loop system for predicting clinical trial outcomes. The approach combines LLM-based structured feature extraction with supervised learning to iteratively improve feature quality and predictive performance.
Methodology

Technical Stack
Models:

Qwen 2.5 7B-Instruct for feature extraction
Lasso Logistic Regression for prediction and feature selection

Feature Engineering:

One-hot encoding for LLM-extracted categorical features
Sentence-BERT embeddings with PCA compression
Unified feature matrix across trials

Evaluation: ROC-AUC for model performance, feature importance for feedback
Key Results
Iteration 1:

ROC-AUC: 0.610
Feature contribution: LLM features 97.2%, embeddings 2.8%
Top categories: study_design, intervention_type, patient_population

Iteration 2:

991 features from 197 trials
Improved hierarchical structure with granular categories
Performance evaluation in progress

Computational Setup
Environment: UIUC Campus Cluster

GPU access via stat queue
Workspace: /scratch/br36
Development: Python, scikit-learn, Transformers, Jupyter

Supplementary: Google Colab Pro for prototyping
Data
Source: ClinicalTrials.gov cancer clinical trials
Note: Data access requires appropriate institutional permissions.
Dependencies
bashpip install transformers torch scikit-learn pandas sentence-transformers
Citation
Research conducted under Professor Ruoqing at UIUC Department of Statistics.
Computational resources: UIUC Campus Cluster.
