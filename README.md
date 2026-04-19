<<<<<<< HEAD
# TKH-26-labs
=======
# Financial Fraud Project
### Caishen Bank



## Overview
For this project I built a machine learning model to detect fraudulent bank transactions for Caishen Bank. I used a dataset of over 6 million synthetic bank transactions to train and evaluate a Random Forest classifier.


## Project Structure

Notebook 1 — EDA:I explored the dataset to find patterns related to fraud and formed a hypothesis

Notebook 2 — Data Cleaning: I cleaned the data, removed unnecessary columns, and engineered new features

Notebook 3 — Model: I trained a Random Forest model and used RandomizedSearchCV to tune it

Report: Written answers to 5 questions about the project



## Model Results

The baseline Random Forest model got an F1 score of 0.9988. After tuning the hyperparameters with RandomizedSearchCV the tuned model got an F1 score of 0.9938. Both scores show the model is very good at detecting fraudulent transactions.



## How to Run

1. Install libraries: `pip install pandas numpy matplotlib seaborn scikit-learn`
2. Add the dataset `Finanacial dataset project.csv` to the project folder
3. Run notebooks in order: Notebook 1 , Notebook 2 , Notebook 3
>>>>>>> cd83c3415908ba574126bd3fa0a1d08de7d1b211
