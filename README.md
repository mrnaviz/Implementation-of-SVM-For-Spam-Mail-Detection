# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the packages# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the necessary python packages using import statements.

2.Read the given csv file using read_csv() method and print the number of contents to be displayed using df.head().

3.Split the dataset using train_test_split.

4.Calculate Y_Pred and accuracy.

5.Print all the outputs.

6.End the Program.

## Program:
```
Program to implement the SVM For Spam Mail Detection..
Developed by: NAVEEN KUMAR B
RegisterNumber: 212222230091
```
```PY
import chardet
file='spam.csv'
with open (file,'rb') as rawdata:
    result = chardet.detect(rawdata.read(100000))
result

import pandas as pd
data=pd.read_csv("spam.csv",encoding='windows-1252')

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
```
## Output:
## Encoding:
![image](https://github.com/harini1006/Implementation-of-SVM-For-Spam-Mail-Detection/assets/113497405/ed87456c-9dd8-418d-a960-1abad11477f2)


## Head():
![image](https://github.com/harini1006/Implementation-of-SVM-For-Spam-Mail-Detection/assets/113497405/8e2c3fec-2fe3-40c3-923a-1a1c3719e734)


## Info():
![image](https://github.com/harini1006/Implementation-of-SVM-For-Spam-Mail-Detection/assets/113497405/b48518c5-c983-44d3-9cc2-14924033aa91)


## isnull().sum():
![image](https://github.com/harini1006/Implementation-of-SVM-For-Spam-Mail-Detection/assets/113497405/50754f89-e886-48c3-a285-44b76317b605)


## Prediction of y:
![image](https://github.com/harini1006/Implementation-of-SVM-For-Spam-Mail-Detection/assets/113497405/8f3a2d63-9aa6-4da2-95c4-d53b87fde998)


## Accuracy:
![image](https://github.com/harini1006/Implementation-of-SVM-For-Spam-Mail-Detection/assets/113497405/d1dcce16-dc32-4ec2-a042-ce25bee461da)


## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.


2. Analyse the data.

3. Use modelselection and Countvectorizer to preditct the values.

4. Find the accuracy and display the result.

## Program:
```
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: NAVEEN KUMAR B
RegisterNumber:  21222230091

import chardet
file = '/content/spam.csv'
with open(file,'rb') as rawdata:
  result = chardet.detect(rawdata.read(100000))
result

import pandas as pd 
data = pd.read_csv("/content/spam.csv",encoding='Windows-1252')

data.head()

data.info()

data.isnull().sum()

x=data["v1"].values

y=data["v2"].values



from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)

from sklearn.feature_extraction.text import CountVectorizer
cv = CountVectorizer()



x_train = cv.fit_transform(x_train)
x_test = cv.transform(x_test)


from sklearn.svm import SVC
svc = SVC()
svc.fit(x_train,y_train)


y_pred = svc.predict(x_test)
y_pred



from sklearn import metrics
accuracy = metrics.accuracy_score(y_test,y_pred)
accuracy
*/
```

## Output:
![image](https://github.com/mrnaviz/Implementation-of-SVM-For-Spam-Mail-Detection/assets/123350791/2cc476b4-f6d0-4b92-8d04-ce3e16d9c838)

data.head():

![image](https://github.com/mrnaviz/Implementation-of-SVM-For-Spam-Mail-Detection/assets/123350791/11a976a2-347f-4373-9e25-861680080d71)

data.info():

![image](https://github.com/mrnaviz/Implementation-of-SVM-For-Spam-Mail-Detection/assets/123350791/cb489095-0be2-41e0-b7c6-8c60a18c1ad9)

data.isnull().sum():

![image](https://github.com/mrnaviz/Implementation-of-SVM-For-Spam-Mail-Detection/assets/123350791/3d638988-b33b-4398-9610-7c35183a52a2)

Accuracy value:

![image](https://github.com/mrnaviz/Implementation-of-SVM-For-Spam-Mail-Detection/assets/123350791/9627ff24-f53a-4365-82d6-e594f213115e)


## Result:

Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
