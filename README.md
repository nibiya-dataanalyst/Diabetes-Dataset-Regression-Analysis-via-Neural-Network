Diabetes Progression Prediction using ANN
An end-to-end Deep Learning regression project built with Python and TensorFlow/Keras. This project models and predicts diabetes disease progression using an Artificial Neural Network (ANN), featuring complete exploratory data analysis (EDA), data scaling, baseline model evaluation, and hyperparameter tuning with regularization.
📌 Table of Contents
Overview

Dataset

Project Pipeline

Model Architecture & Tuning

Results & Evaluation

Installation & Usage

Technologies Used

Overview
The goal of this project is to build a neural network to predict a quantitative measure of diabetes progression one year after baseline, based on ten clinical features.

The project compares two neural network implementations:

Baseline ANN: A minimal single-hidden-layer network.

Improved ANN: A deeper, regularized architecture with L2 regularization, Dropout, and Early Stopping to prevent overfitting and boost generalization performance.

Dataset
The project utilizes the Diabetes Dataset provided by scikit-learn (load_diabetes).

Samples: 442 patients

Features (10 baseline variables):

age: Age in years

sex: Gender

bmi: Body mass index

bp: Average blood pressure

s1–s6: Six blood serum measurements

Target: Quantitative measure of disease progression one year after baseline (ranges from 25 to 346).

Project PipelineData Preprocessing & Safety:Split dataset into training ($80\%$) and testing ($80\%$) sets prior to feature scaling to prevent data leakage.Standardized features using StandardScaler.Explicitly checked and confirmed no missing values exist.

Exploratory Data Analysis (EDA):

Plotted kernel density distribution plots for all features and the target variable.

Generated a full correlation heatmap to analyze relationships between clinical features and disease progression.

Constructed scatter plots with regression lines for key predictive variables (bmi, s5, bp).

Model Development & Training:Baseline ANN: Built with 1 hidden layer (ReLU) and trained using Adam optimizer and MSE loss for 100 epochs.Improved ANN: Built with 3 dense layers, L2 regularization (lambda = 0.01), Dropout(0.2), and an EarlyStopping callback monitored on validation loss.
Evaluation:Metrics recorded on the held-out test set: Mean Squared Error (MSE), Root Mean Squared Error (RMSE), and $R^2$ Score.Visualized training vs. validation loss curves and actual vs. predicted scatter plots.

Model Architecture & Tuning
Improved ANN Architecture
Input Layer (10 Features)
│
├── Dense (64 units, ReLU, L2 Regularization = 0.01)
├── Dropout (Rate = 0.2)
├── Dense (32 units, ReLU, L2 Regularization = 0.01)
├── Dropout (Rate = 0.2)
├── Dense (16 units, ReLU)
└── Output Layer (1 unit, Linear Activation)

Key FindingsThe baseline model showed initial signs of high variance due to the small sample size relative to network capacity.Adding $L2$ regularization and Dropout effectively constrained model parameters, while Early Stopping prevented overfitting by terminating training at the optimal validation loss checkpoint.











