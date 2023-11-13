# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm

### Step 1 :
Import the necessary python packages using import statements.

### Step 2 :
Read the given csv file using read_csv() method and print the number of contents to be displayed using df.head().

### Step 3 :
Split the dataset using train_test_split.

### Step 4 :
Calculate Y_Pred and accuracy.

### Step 5 :
Print all the outputs.

### Step 6 :
End the Program.

## Program:
```

Program to implement the SVM For Spam Mail Detection..
Developed by: Safeeq Fazil.A
RegisterNumber:212222240086

```

```
import pandas as pd
data=pd.read_csv("spam.csv",encoding='latin-1')

data.head()

data.info()

data.isnull().sum()

x=data["EmailText"].values
y=data["Label"].values

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)

from sklearn.feature_extractiaon.text import CountVectorizer
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
```

## Output:

### DATA.HEAD() :

![image](https://github.com/Safeeq-Fazil/Implementation-of-SVM-For-Spam-Mail-Detection/assets/118680361/4257b104-0b14-4d51-8b51-5a8b4d539101)

### DATA.INFO() :

![image](https://github.com/Safeeq-Fazil/Implementation-of-SVM-For-Spam-Mail-Detection/assets/118680361/a00f094a-e002-41b5-ab45-d33cf6e1c241)

### DATA.ISNULL().SUM() :

![image](https://github.com/Safeeq-Fazil/Implementation-of-SVM-For-Spam-Mail-Detection/assets/118680361/29e477f9-ffed-4fdf-b0d2-6649bc60f0ec)

### Y_PRED :

![image](https://github.com/Safeeq-Fazil/Implementation-of-SVM-For-Spam-Mail-Detection/assets/118680361/ad9d4c6c-aa89-4e87-92e8-f1d4c9818634)

### ACCURACY :

![image](https://github.com/Safeeq-Fazil/Implementation-of-SVM-For-Spam-Mail-Detection/assets/118680361/d782819c-1015-4b4a-b226-e546cdef1422)

## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
