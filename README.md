Diabetes Progression Prediction using ANN

This project uses a Artificial Neural Network (ANN) to predict diabetes progression in patients after one year. It compares a simple baseline model with an improved, regularized model to get better results.

What This Project DoesLoads Data: Uses the built-in Diabetes dataset from scikit-learn.Cleans & Preprocesses Data: Checks for missing values and scales all features using StandardScaler.Explores Data (EDA): Plots graphs and correlation heatmaps to understand how clinical features relate to disease progression.Builds & Trains Models:Baseline Model: A simple single-layer neural network.Improved Model: A deeper network with extra techniques (Dropout, L2 Regularization, and Early Stopping) to avoid overfitting.Evaluates Results: Compares both models using Mean Squared Error (MSE) and R2 Score.


Dataset Details
Total Samples: 442 patients

Features: 10 clinical attributes (age, sex, body mass index, blood pressure, and 6 blood serum measurements)

Target: A number measuring diabetes progression after one year
