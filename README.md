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
Developed by:Abdul kadher S
Register Number:212225230002 
```
```python

import numpy as np 
import matplotlib.pyplot as plt
x = np.array([0,1,2,3,4,5,6,7,8,9])
y = np.array([1,3,2,5,7,8,8,9,10,12])
plt.scatter(x,y)
plt.show()
xmean = np.mean(x)
ymean = np.mean(y)
num=0
den=0
for i in range(len(x)):
    num+=(x[i]-xmean)*(y[i]-ymean)
    den+=(x[i]-xmean)**2
m = num/den
b = ymean - m*xmean
print(m,b)
ypred = m*x+b
print(ypred)

plt.scatter(x,y,color='Red')
plt.plot(x,ypred,color='Blue')
plt.show()
```

## Output
<img width="817" height="589" alt="AdobeExpressPhotos_b87aea3cffc449398230e7b0bab0c5c1_CopyEdited" src="https://github.com/user-attachments/assets/50e92f73-daa4-492e-8fea-250da6ced494" />
<img width="764" height="515" alt="AdobeExpressPhotos_24855787d30d42edaa21d6e93ac22dde_CopyEdited" src="https://github.com/user-attachments/assets/13071478-1dd3-47af-9c2b-fe13031b94ca" />


## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
