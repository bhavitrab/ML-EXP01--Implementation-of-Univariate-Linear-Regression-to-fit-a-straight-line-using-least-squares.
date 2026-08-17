<h1>Implementation of Univariate Linear Regression</h1>

<h3>AIM:</h3>
To implement univariate Linear Regression to fit a straight line using least squares.

<h3>Equipments Required:</h3>
1.Hardware – PCs
2.Anaconda – Python 3.7 Installation / Jupyter notebook

<h3>Algorithm</h3>
1.Get the independent variable X and dependent variable Y.
2.Calculate the mean of the X -values and the mean of the Y -values.
3.Find the slope m of the line of best fit using the formula.
<img width="487" height="110" alt="image" src="https://github.com/user-attachments/assets/22eb7bbf-ab4a-419d-b389-e0d20cbfe226" />


4. Compute the y -intercept of the line by using the formula:
<img width="412" height="61" alt="image" src="https://github.com/user-attachments/assets/eb554420-3f50-4b57-8288-c2286564986a" />


6. Use the slope m and the y -intercept to form the equation of the line. 6. Obtain the straight line equation Y=mX+b and plot the scatterplot.
Program and Output:
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: BHAVITRA B
RegisterNumber: 212225040047

*/
```
import numpy as np
import matplotlib.pyplot as plt

#GETTING INPUT
x = np.array(eval(input()))#EXAMPLE INPUT - 2,9,5,5,3,7,1,8,6,2
y = np.array(eval(input()))#EXAMPLE INPUT - 69,98,82,77,71,84,55,94,84,64

#FINDING MEAN 
x_mean = np.mean(x)
y_mean = np.mean(y)

#CALCULATING NUMERATOR AND DENOMINATOR
num = 0
denom = 0
for i in range(len(x)):
    num += (x[i] - x_mean) * (y[i] - y_mean)
    denom += (x[i] - x_mean) ** 2
m = num / denom

b = y_mean - m * x_mean
print(m, b)

#FINDING Y-PREDICTED
y_predicted = m * x + b
print(y_predicted)

#PLOTTING GRAPH
plt.scatter(x, y)
plt.plot(x, y_predicted, color='red')
plt.show()
```
<h3>output</h3>
<img width="883" height="523" alt="image" src="https://github.com/user-attachments/assets/98151717-3c4c-48a4-bf82-992a5b029f41" />


Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
