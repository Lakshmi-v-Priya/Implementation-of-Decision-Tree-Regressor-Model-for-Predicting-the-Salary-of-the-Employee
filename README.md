# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the standard libraries.

2.Upload the dataset and check for any null values using .isnull() function.

3.Import LabelEncoder and encode the dataset.

4.Import DecisionTreeRegressor from sklearn and apply the model on the dataset.

5.Predict the values of arrays.

6.Import metrics from sklearn and calculate the MSE and R2 of the model on the dataset.

7.Predict the values of array.

8.Apply to new unknown values.

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: Lakshmi Priya .V
RegisterNumber:  212223220049
*/
```
```
import pandas as pd
data = pd.read_csv("Salary.csv")
data.head()
data.info()
data.isnull().sum()
from sklearn.preprocessing import LabelEncoder
le = LabelEncoder()
data["Position"] = le.fit_transform(data["Position"])
data.head()
x = data[["Position", "Level"]]
y = data["Salary"]
from sklearn.model_selection import train_test_split
x_train, x_test, y_train, y_test = train_test_split(x, y, test_size=0.2)
from sklearn.tree import DecisionTreeRegressor
dt = DecisionTreeRegressor()
dt.fit(x_train, y_train)
y_pred = df.predict(x_test)
from sklearn import metrics
mse = metrics.mean_squared_error(y_test, y_pred)
mse
r2 = metrics.r2_score(y_test, y_pred)
r2
dt.predict([[5,6]])
```

## Output:
![image](https://github.com/user-attachments/assets/c048a389-6060-4aa1-9a91-3ff24f48527e)
![image](https://github.com/user-attachments/assets/a654279c-941b-4fee-adb0-db6d0aad8af5)
![image](https://github.com/user-attachments/assets/8c3a17d9-4015-4426-88e4-a227606d140a)
![image](https://github.com/user-attachments/assets/1fd09751-544a-4095-b319-4e2f0d218a68)
![image](https://github.com/user-attachments/assets/981b881d-0667-44e5-8857-d501572cf619)
![image](https://github.com/user-attachments/assets/253e1ae8-19b0-4643-a99c-cd7e08bc6ddb)
![image](https://github.com/user-attachments/assets/20ae79c3-5038-4ade-b4d0-3ef72255286e)


## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
