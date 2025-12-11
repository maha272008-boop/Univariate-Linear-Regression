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


![first](https://github.com/user-attachments/assets/46593bd3-129e-4c9f-b661-dd8c7bb328cd)


![second](https://github.com/user-attachments/assets/5092531b-a7fb-4bc2-ac10-e4510fbab8d4)


![third](https://github.com/user-attachments/assets/d84f5438-a53d-4b87-85f7-157813a2d31f)


![four](https://github.com/user-attachments/assets/b35ff4cd-e19f-478d-9118-ac79ea0189a9)


![five](https://github.com/user-attachments/assets/14195b1c-6bcc-4960-be31-e9cffe0b3752)




## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
