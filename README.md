# Implementation of Univariate Linear Regression
## Aim:
To implement univariate Linear Regression to fit a straight line using least squares.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
1.	Get the independent variable X and dependent variable Y.
2.	Calculate the mean of the X -values and the mean of the Y -values.
3.	Find the slope m of the line of best fit using the formula.
 ![eqn1](./eq1.jpg)
4.	Compute the y -intercept of the line by using the formula:
![eqn2](./eq2.jpg)  
5.	Use the slope m and the y -intercept to form the equation of the line.
6.	Obtain the straight line equation Y=mX+b and plot the scatterplot.
## Program
# Register Number:25017569
# Developed by:Vijiyalakshmi A
```
import numpy as np
import matplotlib.pyplot as plt
X= np.array([0,1,2,3,4,5,6,7,8,9])
Y= np.array([1,3,2,5,7,8,8,9,10,12])
plt.scatter(X,Y)
plt.show()
X_Mean=np.mean(X)
Y_Mean=np.mean(Y)
num=0
den=0
for i in range(len(X)):
    num+=(X[i]-X_Mean)*(Y[i]-Y_Mean)
    den+=(X[i]-X_Mean)**2

m=num/den
b=Y_Mean-(m*X_Mean)
print(f"Slope : {m}\nIntercept : {b}")
Y_Pred=(m*X)+b
print(f"Predicted values are : \n{Y_Pred}")
plt.scatter(X,Y,color='Red')
plt.plot(X,Y_Pred,color='Blue')
plt.show()

```
## Output
<img width="1046" height="132" alt="Screenshot 2025-12-11 192209" src="https://github.com/user-attachments/assets/c729311a-2371-439e-bce1-f804c06684a1" />
<img width="539" height="374" alt="Screenshot 2025-12-11 192229" src="https://github.com/user-attachments/assets/b0aab97f-7da5-4251-854e-335a83fc005c" />
<img width="1046" height="355" alt="Screenshot 2025-12-11 192249" src="https://github.com/user-attachments/assets/3142126d-c643-4e64-9b52-217d2e60a6af" />
<img width="1062" height="91" alt="Screenshot 2025-12-11 192304" src="https://github.com/user-attachments/assets/fd49ca56-33d5-4b08-91ff-b2ea2fe074b8" />
<img width="575" height="404" alt="Screenshot 2025-12-11 192319" src="https://github.com/user-attachments/assets/3dfe7346-39ff-4e9c-a031-db7cbec41a68" />

## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
