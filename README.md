# EXPERIMENT-09
# IMPLEMENTATION OF UNIVARIATE LINEAR REGRESSION

## AIM :

To implement univariate Linear Regression to fit a straight line using least squares.

## EQUIPMENTS REQUIRED :

-	Hardware – PCs
-	Anaconda – Python 3.7 Installation / Moodle-Code Runner

## ALGORITHIM :

1.	Get the independent variable X and dependent variable Y.
2.	Calculate the mean of the X -values and the mean of the Y -values.
3.	Find the slope m of the line of best fit using the formula.  
![eqn1](./eq1.jpg)
4.	Compute the y -intercept of the line by using the formula:  
![eqn2](./eq2.jpg)  
5.	Use the slope m and the y -intercept to form the equation of the line.
6.	Obtain the straight line equation Y=mX+b and plot the scatterplot.
## PROGRAM :

```python
# Register No: 22008311
# Developed By: MIDHUN AZHAHU RAJA P
import numpy as np
import matplotlib.pyplot as plt
X = np.array(eval(input()))
Y = np.array(eval(input()))
Xmean = np.mean(X)
Ymean = np.mean(Y)
num, den = 0, 0
for i in range(len(X)):
    num += (X[i]-Xmean)*(Y[i]-Ymean)
    den += (X[i]-Xmean)**2
m = num/den
c = Ymean-m*Xmean
print(m, c)
Y_pred = m*X+c
print(Y_pred)
plt.scatter(X, Y)
plt.plot(X, Y_pred, color="red")
plt.show()



```
## OUTPUT :
![output2](https://user-images.githubusercontent.com/118054670/214352372-e5f19da4-5e6d-48fa-9dba-bf3a873d743e.png)
![output1](https://user-images.githubusercontent.com/118054670/214352418-07e34b79-d41a-4128-abc9-fa98ca836f23.png)


## RESULT :

Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
