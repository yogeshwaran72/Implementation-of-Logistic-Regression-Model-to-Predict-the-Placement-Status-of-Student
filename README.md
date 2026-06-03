# Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student

## AIM:
To write a program to implement the the Logistic Regression Model to Predict the Placement Status of Student.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Load the dataset, drop unnecessary columns, and encode categorical variables.

2.Define the features (X) and target variable (y).

3.Split the data into training and testing sets.

4.Train the logistic regression model, make predictions, and evaluate using accuracy and other

## Program:
```
/*

import pandas as pd
from sklearn.preprocessing import LabelEncoder
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LogisticRegression
from sklearn.metrics import accuracy_score, classification_report

data = pd.read_csv(r"C:\Users\admin\Downloads\Placement_Data.csv")

print(data.head())

data1 = data.copy()

data1 = data1.drop(["sl_no", "salary"], axis=1)

print(data1.head())

print("Missing Values")
print(data1.isnull().sum())

print("Duplicate Rows")
print(data1.duplicated().sum())

le = LabelEncoder()

data1["gender"] = le.fit_transform(data1["gender"])
data1["ssc_b"] = le.fit_transform(data1["ssc_b"])
data1["hsc_b"] = le.fit_transform(data1["hsc_b"])
data1["hsc_s"] = le.fit_transform(data1["hsc_s"])
data1["degree_t"] = le.fit_transform(data1["degree_t"])
data1["workex"] = le.fit_transform(data1["workex"])
data1["specialisation"] = le.fit_transform(data1["specialisation"])
data1["status"] = le.fit_transform(data1["status"])

print(data1.head())

x = data1.iloc[:, :-1]

y = data1["status"]

x_train, x_test, y_train, y_test = train_test_split(
    x,
    y,
    test_size=0.2,
    random_state=0
)

lr = LogisticRegression(solver="liblinear")

lr.fit(x_train, y_train)

y_pred = lr.predict(x_test)

print("Predicted Values")
print(y_pred)

accuracy = accuracy_score(y_test, y_pred)

print("Accuracy =", accuracy)

report = classification_report(y_test, y_pred)

print("Classification Report")
print(report)

new_data = pd.DataFrame(
    [[1, 80, 1, 90, 1, 1, 90, 1, 0, 85, 1, 85]],
    columns=x.columns
)
result = lr.predict(new_data)
print("Prediction =", result)

*/
```

## Output:
<img width="952" height="732" alt="image" src="https://github.com/user-attachments/assets/15564bdb-fc71-47a3-ad00-54fef6fed43a" />

<img width="971" height="490" alt="image" src="https://github.com/user-attachments/assets/4599e079-f559-4341-94bb-43072430c40f" />


## Result:
Thus the program to implement the the Logistic Regression Model to Predict the Placement Status of Student is written and verified using python programming.
