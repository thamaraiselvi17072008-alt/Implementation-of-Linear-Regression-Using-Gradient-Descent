# Implementation-of-Linear-Regression-Using-Gradient-Descent

## AIM:
To write a program to predict the profit of a city using the linear regression model with gradient descent.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the required library and read the dataframe.

2.Write a function compute Cost to generate the cost function.

3.Perform iterations of gradient steps with learning rate.

4.Plot the Cost function using Gradient Descent and generate the required graph.

## Program:
```
/*
Program to implement the linear regression using gradient descent.
Developed by:THAMARAISELVI.V
RegisterNumber: 212225040467
/*

import numpy as np
import pandas as pd
import matplotlib.pyplot as plt

data=pd.read_csv("startup.csv")

C=data['R&D Spend'].values
d=data['Profit'].values

C=(C-C.mean())/C.std()

m=0
b=0

learning_rate=0.01
epochs=1000
n=len(C)

for i in range(epochs):
    d_pred=m*C+b
    
    dm=(-2/n)*np.sum(C*(d-d_pred))
    db=(-2/n)*np.sum(d-d_pred)
    
    m=m-learning_rate*dm
    b=b-learning_rate*db
    
print("Slope(m):",m)
print("Intercept(b):",b)
    
d_pred=m*C+b
    
plt.scatter(C,d)
plt.plot(C,d_pred)
plt.xlabel("R&D Spend (Normalised)")
plt.ylabel("profit")
plt.title("Gradient Descent on 50_Startups Dataset")

plt.show()

```

## Output:

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/e395a4f4-6a0a-48f2-87f2-e16cba6da2e0" />


## Result:
Thus the program to implement the linear regression using gradient descent is written and verified using python programming.
