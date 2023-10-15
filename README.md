# # Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee
AIM:

To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
# Equipments Required:

    1. Hardware – PCs
    2. Anaconda – Python 3.7 Installation / Jupyter notebook

# Algorithm

1.Import the libraries and read the data frame using pandas.

2.Calculate the null values present in the dataset and apply label encoder.

3.Determine test and training data set and apply decison tree regression in dataset.

4.Calculate Mean square error,data prediction and r2.
# Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: Agalya R
RegisterNumber:212222040003

import pandas as pd
data=pd.read_csv("/content/Salary.csv")

data.head()

data.info()

data.isnull().sum()

from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()

x=data[["Position","Level"]]
y=data["Salary"]

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=2)


from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)

from sklearn import metrics
mse=metrics.mean_squared_error(y_test,y_pred)
mse

r2=metrics.r2_score(y_test,y_pred)
r2

dt.predict([[5,6]])
  
*/
```

# Output:
# data.head()
![image](https://github.com/AGALYARAMESHKUMAR/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119394395/bfbabcd4-c277-4abe-a80b-bcf1a519dbcb)

# data.info()
![image](https://github.com/AGALYARAMESHKUMAR/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119394395/d66bfc37-58a6-44cf-8335-f3e5815aecee)

# isnull() and sum()
![image](https://github.com/AGALYARAMESHKUMAR/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119394395/72a2fbb0-0a39-4ec0-829d-3f531fb9bacb)

# data.head() for salary
![image](https://github.com/AGALYARAMESHKUMAR/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119394395/ff11cd77-995f-4a19-a875-6ea65ce49656)

# MSE value
![image](https://github.com/AGALYARAMESHKUMAR/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119394395/ada24989-35af-416f-8769-73e4f598e882)

# r2 value
![image](https://github.com/AGALYARAMESHKUMAR/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119394395/52f8ad2c-9962-48e5-81c0-eb609ce5d89b)

# data prediction
![image](https://github.com/AGALYARAMESHKUMAR/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119394395/61c77d78-2155-48e0-b254-6480b53a998b)

# Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
