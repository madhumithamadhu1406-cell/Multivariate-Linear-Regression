# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step1
<br>

### Step2
<br>

### Step3
<br>

### Step4
<br>

### Step5
<br>

## Program:
```
import matplotlib.pyplot as plt
import numpy as np
from sklearn import linear_model
from sklearn.datasets import load_diabetes
from sklearn.model_selection import train_test_split

# Load dataset
data = load_diabetes()
X = data.data
y = data.target

# Split dataset
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.4, random_state=1
)

# Model
reg = linear_model.LinearRegression()
reg.fit(X_train, y_train)

print("Coefficients:", reg.coef_)
print("Variance score:", reg.score(X_test, y_test))

plt.scatter(reg.predict(X_train), reg.predict(X_train) - y_train,
            color="green", s=10, label="Train data")

plt.scatter(reg.predict(X_test), reg.predict(X_test) - y_test,
            color="blue", s=10, label="Test data")

plt.hlines(y=0, xmin=0, xmax=400, linewidth=2)

plt.legend(loc="upper right")
plt.title("Residual Errors")
plt.show()








```
## Output:
![WhatsApp Image 2026-03-18 at 11 31 43 AM](https://github.com/user-attachments/assets/3824a6d3-3f1b-46ba-8fb5-9452fcf59631)
![WhatsApp Image 2026-03-18 at 11 32 25 AM](https://github.com/user-attachments/assets/29e542b2-d392-4012-af7c-5bc77e9975b6)

## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
