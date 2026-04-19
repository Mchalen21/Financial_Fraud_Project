# Financial Fraud Project Report



## Question 1: Which insights did you gain from your EDA?

After exploring the data I found a few important things:

- Only 0.13% of transactions are fraud which means the dataset is very imbalanced
- Fraud only happens in TRANSFER and CASH_OUT transactions
- Fraudulent transactions involve much higher amounts of money than normal ones
- When the origin account balance is drained to zero after a transaction, it is usually fraud
- The isFlaggedFraud column barely catches any real fraud so I removed it



## Question 2: How did you determine which columns to drop or keep?

I dropped three columns based on what I found in the EDA:

- nameOrig and nameDest, these are just account ID numbers and the model cannot learn anything useful from them
- isFlaggedFraud, this column catches almost no real fraud and could confuse the model

I kept all the balance and amount columns because they showed clear differences between fraud and non fraud transactions.



## Question 3: Which hyperparameter tuning strategy did you use and why?

I used RandomizedSearchCV because the dataset has over 6 million rows and GridSearchCV would have taken too long to run. RandomizedSearchCV tries a smaller number of combinations and still finds good results in much less time.



## Question 4: How did your model's performance change after tuning?

Both models performed very well. The baseline model got an F1 score of 0.9988 and the tuned model got 0.9938. The scores are very close because the model was already performing well before tuning. The tuning helped confirm the best settings for the model.



## Question 5: What was your final F1 Score?

- Baseline F1 Score: 0.9988
- Tuned F1 Score: 0.9938
- Best Parameters: n_estimators=100, max_depth=10, max_features=sqrt

Both scores show that the model is very good at detecting fraudulent transactions.
