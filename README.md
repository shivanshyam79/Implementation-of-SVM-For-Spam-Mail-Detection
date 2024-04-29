# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the necessary packages.
2. Read the given csv file and display the few contents of the data.
3. Assign the features for x and y respectively.
4. Split the x and y sets into train and test sets.
5. Convert the Alphabetical data to numeric using CountVectorizer.
6. Predict the number of spam in the data using SVC (C-Support Vector Classification) method of SVM (Support vector machine) in sklearn library.
7. Find the accuracy of the model.

## Program:
```
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: shyam R
RegisterNumber:212223040200
import pandas as pd
data=pd.read_csv("spam.csv",encoding='latin-1')

data.head()

data.info()

data.isnull().sum()

x=data["v1"].values
y=data["v2"].values

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)

from sklearn.feature_extraction.text import CountVectorizer
cv=CountVectorizer()

x_train=cv.fit_transform(x_train)
x_test=cv.transform(x_test)

from sklearn.svm import SVC
svc=SVC()
svc.fit(x_train,y_train)

y_pred=svc.predict(x_test)
y_pred

from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy
  
*/
```

## Output:
## data.head()
![279768985-f25a1488-2cf4-401c-b9a1-c718528f7009](https://github.com/shivanshyam79/Implementation-of-SVM-For-Spam-Mail-Detection/assets/151513860/a43cf659-573b-406c-9cb9-eb9ef4cf2696)
## data.info()
![279769009-701258ca-4918-4d2f-b242-e292c007eb6b](https://github.com/shivanshyam79/Implementation-of-SVM-For-Spam-Mail-Detection/assets/151513860/da144b87-e449-4ce1-b9d5-90d8d4f4a76e)
## data.isnull().sum()
![279769021-f630a7bd-8b5b-4a6b-9339-efc41656d1a6](https://github.com/shivanshyam79/Implementation-of-SVM-For-Spam-Mail-Detection/assets/151513860/ce7e6f24-b69b-4ffa-8472-66f85ea79336)
## y_prediction value
![279769054-9f5f562a-6191-47cd-a533-57677ea21f50](https://github.com/shivanshyam79/Implementation-of-SVM-For-Spam-Mail-Detection/assets/151513860/5d855521-6a41-497e-b3a7-65f713d15168)
## Accuracy value
![279769089-22fc6d5f-3a59-4a8f-bf6e-5cc76de836a0](https://github.com/shivanshyam79/Implementation-of-SVM-For-Spam-Mail-Detection/assets/151513860/07b38839-c8be-493c-bc05-57f520f1179a)

## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
