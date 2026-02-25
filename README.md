# BLENDED_LEARNING
# Implementation of Logistic Regression Model for Classifying Food Choices for Diabetic Patients

## AIM:
To implement a logistic regression model to classify food items for diabetic patients based on nutrition information.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. 
2. 
3. 
4. 

## Program:
```
/*
Program to implement Logistic Regression for classifying food choices based on nutritional information.
Developed by: Dhinesh kumar
RegisterNumber: 212225240036
import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LogisticRegression
from sklearn.preprocessing import LabelEncoder, MinMaxScaler
from sklearn.metrics import accuracy_score, classification_report, confusion_matrix
import matplotlib.pyplot as plt

# Load the dataset
df = pd.read_csv("food_items (1).csv")

# Inspect the dataset
print("Name:Dhinesh Kumar ")
print("Reg. No:212225240036")
print("Dataset Overview:")
print(df.head())
print("\nDataset Info:")
print(df.info())

X_raw = df.iloc[:, :-1]
y_raw = df.iloc[:, -1:]

scaler = MinMaxScaler()
X = scaler.fit_transform(X_raw)

label_encoder = LabelEncoder()
y = label_encoder.fit_transform(y_raw.values.ravel())

# Split the dataset
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, stratify=y, random_state=123
)

# Model parameters
penalty = 'l2'
multi_class = 'multinomial'
solver = 'lbfgs'
max_iter = 1000

# Define logistic regression model
l2_model = LogisticRegression(
    random_state=123,
    penalty=penalty,
    multi_class=multi_class,
    solver=solver,
    max_iter=max_iter
)

l2_model.fit(X_train, y_train)

y_pred = l2_model.predict(X_test)

# Evaluate the model
print("\nModel Evaluation:")
print("Accuracy:", accuracy_score(y_test, y_pred))
print("\nClassification Report:")
print(classification_report(y_test, y_pred))

# Confusion Matrix
conf_matrix = confusion_matrix(y_test, y_pred)
print(conf_matrix)
*/
```

## Output:
<img width="1353" height="658" alt="image" src="https://github.com/user-attachments/assets/4f0293ff-dae6-4c12-961d-bc608dd0d4f0" />
<img width="1344" height="660" alt="image" src="https://github.com/user-attachments/assets/50ad98e4-4304-4afc-982d-6a5b92898dc3" />
<img width="1293" height="377" alt="image" src="https://github.com/user-attachments/assets/8139f550-abcc-4ace-aa21-aab0c23dfde7" />


## Result:
Thus, the logistic regression model was successfully implemented to classify food items for diabetic patients based on nutritional information, and the model's performance was evaluated using various performance metrics such as accuracy, precision, and recall.
