🌍 Flag Classification using Decision Trees

This project applies a Decision Tree Classifier to distinguish between European and Oceania national flags using visual and symbolic characteristics such as colors, patterns, and shapes.

The goal is to demonstrate a complete machine learning workflow including data preprocessing, model training, hyperparameter tuning, pruning, and visualization — all in a clean, reproducible Jupyter Notebook.

📌 Project Objective

Analyze differences between flags from Europe and Oceania

Train a Decision Tree classification model

Tune max_depth to control model complexity

Apply cost-complexity pruning (ccp_alpha) to reduce overfitting

Visualize decision trees for interpretability

📊 Dataset

Name: Flags Dataset

Source: UCI Machine Learning Repository

Link: https://archive.ics.uci.edu/ml/machine-learning-databases/flags/

Target Variable

landmass

3 → Europe

6 → Oceania

Features Used

Only numeric and binary features were used to allow statistical aggregation and modeling:

Colors: red, green, blue, gold, white, black, orange

Patterns & Symbols: bars, stripes, circles, crosses, saltires, quarters, sunstars, triangle, animate

⚠️ Categorical features such as mainhue were intentionally excluded from mean calculations to avoid type errors.

🧠 Technologies & Libraries

Python

Pandas

NumPy

Matplotlib

Scikit-learn

Jupyter Notebook

⚙️ Methodology

Data Loading & Cleaning

Loaded dataset from UCI repository

Filtered rows for Europe and Oceania

Exploratory Data Analysis

Examined distribution of countries by landmass

Calculated average flag features per landmass

Model Training

Split data into training and test sets (60/40)

Trained Decision Tree classifiers with varying max_depth

Hyperparameter Tuning

Selected optimal tree depth based on test accuracy

Applied cost-complexity pruning (ccp_alpha)

Model Evaluation & Visualization

Plotted accuracy vs depth and pruning strength

Visualized final decision tree for interpretability

📈 Results

Decision Trees were able to classify flags with strong accuracy based on visual features alone

Shallow trees generalized better than very deep trees

Pruning further improved model robustness and interpretability

🎯 Key Learning Outcomes

Handling mixed data types in pandas

Understanding overfitting in Decision Trees

Applying pruning techniques

Interpreting tree-based ML models
