# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm

~~~
1.Import the necessary packages using import statement.
2.Read the given csv file and print the number of contents to be displayed. 
3.Split the dataset using train_test_split.
4.Calculate Y_Pred and accuracy.
5.Display the result

~~~



## Program:
```
Program to implement the SVM For Spam Mail Detection..
Developed by: kathirvel.A
```



```
RegisterNumber:  212221230047
import pandas as pd
data=pd.read_csv("spam.csv",encoding='latin-1')
data.head()
data.info()
data.isnull().sum()
x=data["EmailText"].values
y=data["Label"].values
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

data.head()



![image](https://user-images.githubusercontent.com/94911373/173280215-ab07ba14-be28-488e-adf6-2afd781193d9.png)




![image](https://user-images.githubusercontent.com/94911373/173280239-d1f0e4b6-1f91-4baa-8e47-3199d5a11a34.png)


data.info()


![image](https://user-images.githubusercontent.com/94911373/173280266-5bf3afb7-922c-4210-9445-ffa05163682a.png)


Data.isnull().sum()



![image](https://user-images.githubusercontent.com/94911373/173280381-0a7766da-c1ae-412b-a7f4-93676dfcce6b.png)




y_pred


![image](https://user-images.githubusercontent.com/94911373/173280434-f428cbf1-2680-417f-aa72-b4a1fb961475.png)




accuracy


![image](https://user-images.githubusercontent.com/94911373/173280531-5507a95f-acfa-44a7-8b37-020e69726b2c.png)



## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
