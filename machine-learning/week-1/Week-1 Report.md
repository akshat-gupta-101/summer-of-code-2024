# Week-1 Report

Dataset used: [https://www.kaggle.com/datasets/rupakroy/online-payments-fraud-detection-dataset](https://www.kaggle.com/datasets/rupakroy/online-payments-fraud-detection-dataset)

### Approach:

During EDA, I found that there were a few columns which needed to be dropped as they were not necessary and some columns required one-hot encoding to be done because algorithms handle numerical values better than strings. Then I normalized the data and then split it into training set and test set with a test_size = 0.2. I also used a cross-validation set for evauating Logistic Regression Model in which the train : cv : test split was 0.6 : 0.2 : 0.2. Then I implemented the following 6 algorithms:

- Logistic Regression
- Random Forest
- XGBoost
- LightGBM
- Support Vector Machine
- Neural Network

 and tried to optimize them and then evaluated them using reliability metric such as precision, recall, f1 score, confusion matrix, precision-recall score, ROC AUC score. 

### Challenges:

The dataset had huge class-imbalance so I did under-sampling to tackle that issue. Also I did not know anything about LightBGM, and SVM so I had to learn how those algorithms worked and then also learnt how to implement them so this was I believe one of the factors because of which it took me a bit too long to make this submission but I think it was worth it. 

### Results:

Turns out that **LightGBM** algorithm worked the best in my case. 

F1 Scores:

1. Logistic Regression: 0.8274809160305343
2. Random Forest: 0.9931423961274708
3. XGBoost: 0.9903303787268333
4. LightGBM: 0.99
5. Support Vector Machine: 0.8390705679862306
6. Neural Network: 0.9771726071285542

Precision-Recall Score score:

1. Logistic Regression: 0.92
2. Random Forest: 0.99818
3. XGBoost: 0.99850
4. LightGBM: 0.99929
5. Support Vector Machine: 0.93873
6. Neural Network: 0.99929

Accuracy:

1. Logistic Regression:  0.8165584415584416
2. Random Forest: 0.9931006493506493
3. XGBoost: 0.9902597402597403
4. LightGBM: 0.9943
5. Support Vector Machine: 0.8482142857142857
6. Neural Network: 0.9768668831168831