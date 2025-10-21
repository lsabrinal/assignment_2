Overview: I built a Logistic Regression model with a full ML pipeline in order to predict the likelihood of someone getting a stroke based on variables related to demographic and health.

For my model pipeline, I first cleaned my data. I filled in missing values in the BMI column with median values of the training set, and values in the smoker column with unknown. With my categorical columns such as gender, I utilized one-hot encoding to avoid multicollinearity. I also used the standard scalar package to standarize numeric columns. After moving on I realized this was not enough to set up the data, as I had trouble with columns not aligning between the test and train data, so then I went back to reindex my columns. I also made sure to drop the target column here (stroke) from training, as well as the id column which was giving me issues but was not necessary for the model.

I used a simple logistic regression to see how well it would perform on the data, and used an 80/20 split. I also realized that the stroke variable has a weigh imbalance due to how much of the data was 0, so I made sure to account for this. 

My evaluation metrics were:
  Accuracy: 0.7839934667211107
  Precision: 0.13851351351351351
  Recall: 0.8118811881188119
  F1 Score: 0.23665223665223664
  ROC AUC: 0.8699630610420497

Noting the low very precision, and that there are likely many false positives which accounts for my low score on kaggle as well. 

Takeaways: I mainly learned a lot through the cleaning steps where I had to troubleshoot my steps multiple times due to errors being caused by columns like ID, and the test and training data not aligning which made it difficult to build my model. I understand that cleaning the data and setting it up can really be the hardest part. On the other hand, I also became more familiar using github and pushing changes through, as well as setting up a (hopefully) correct structure as I failed to do so previously. This was an insightful assignment and I look forward to learning some better models to improve my score if we revisit this challenge.
