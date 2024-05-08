# EX:5 DATA VISUALIZATION USING MATPLOT LIBRARY

# Aim:
  To Perform Data Visualization using matplot python library.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:

```
NAME: SATHISH R
REGNO: 212222100048
```

### TO CAPTURE A TREND
### 1.Line Chart
```
import matplotlib.pyplot as plt
import numpy as np
x=[0,1,2,3,4,5]
y=[0,1,4,9,16,25]
plt.plot(x,y)
plt.show()
```
![5-1](https://github.com/Divya110205/EXNO-5-DS/assets/119404855/ce370ad1-af72-48f0-9c97-4c09ba565ae4)

### 2.Multi-Line Chart
```
x1=[1,2,3]
y1=[2,4,1]
plt.plot(x1,y1,label="line 1")
x2=[1,2,3]
y2=[4,1,3]
plt.plot(x2,y2,label="line 2")
plt.xlabel('x-axis')
plt.ylabel('y-axis')
plt.title('Multi-Line Chart')
plt.legend()
plt.show()
```
![5-2](https://github.com/Divya110205/EXNO-5-DS/assets/119404855/26a35601-9aa9-4983-b37c-bd580e66f940)

### 3.Area Chart
```
x=[1,2,3,4,5]
y1=[10,12,14,16,18]
y2=[5,7,9,11,13]
y3=[2,4,6,8,10]
plt.fill_between(x,y1,color='blue')
plt.fill_between(x,y2,color='green')
plt.plot(x,y1,color='red')
plt.plot(x,y2,color='black')
plt.legend(['y1','y2'])
plt.show()
```
![5-3](https://github.com/Divya110205/EXNO-5-DS/assets/119404855/63883d6c-d1ea-44f4-90f9-23130d624a6d)

### 4.Stacked Area Chart
```
plt.stackplot(x,y1,y2,y3,labels=['Line 1','Line 2','Line 3'])
plt.legend(loc='upper left')
plt.title('Stacked Line Chart')
plt.xlabel('X-axis')
plt.ylabel('Y-axis')
plt.show()
```
![5-4](https://github.com/Divya110205/EXNO-5-DS/assets/119404855/257053a3-9927-48c9-acac-c5ef778630e9)

### 5.Spline Chart
```
from scipy.interpolate import make_interp_spline
x=np.array([1,2,3,4,5,6,7,8,9,10])
y=np.array([2,4,5,7,8,8,9,10,11,12])
spl=make_interp_spline(x,y)
x1=np.linspace(x.min(),x.max(),100)
y1=spl(x1)
plt.plot(x,y,'*',label='data')
plt.plot(x1,y1,'-',label="spline")
plt.legend()
plt.show()
```
![5-5](https://github.com/Divya110205/EXNO-5-DS/assets/119404855/052795a4-7ab1-48a3-9e18-16bd30f17142)

### TO VISUALIZE RELATIONSHIPS
### 1.Bar Chart
```
val=[5,6,3,7,2]
names=["A","B","C","D","E"]
plt.bar(names,val,color="blue")
plt.show()
```
![5-6](https://github.com/Divya110205/EXNO-5-DS/assets/119404855/39bbd8d3-a82f-49bd-9c8f-13037dfdb978)

### 2.Scatter Plot
```
x=[0,1,2,3,4,5]
y=[0,1,4,9,16,25]
plt.scatter(x,y,s=30,color="red")
plt.show()
```
![5-7](https://github.com/Divya110205/EXNO-5-DS/assets/119404855/8f67a4bb-03ad-4c64-903c-453ca8760169)

### 3.Bubble Chart
```
x = [1, 2, 3, 4, 5]
y = [10, 15, 20, 25, 30]
sizes = [100, 200, 300, 400, 500]
plt.scatter(x, y, s=sizes, alpha=0.5)
plt.xlabel('x_values')
plt.ylabel('y_values')
plt.title('Bubble Chart')
plt.show()
```
![5-8](https://github.com/Divya110205/EXNO-5-DS/assets/119404855/212820b5-2e8e-4796-83ac-7827b2d94c37)

### TO CAPTURE DISTRIBUTIONS
### 1.Histogram
```
ages=[2,5,70,40,30,45,50,45,43,40,44,60,7,13,57,18,90,77,32,21,20,40]
range=(0,100)
bins=10
plt.hist(ages,bins,range,color='purple',histtype='bar',rwidth=0.8)
plt.xlabel('age')
plt.ylabel('No. Of People')
plt.title('Histogram')
plt.show()
```
![5-9](https://github.com/Divya110205/EXNO-5-DS/assets/119404855/a8145747-78d1-40c8-a581-496e5fd3d4e3)

### 2.Box Plot
```
np.random.seed(0)
data=np.random.normal(loc=0,scale=1,size=100)
data
fig,ax=plt.subplots()
ax.boxplot(data)
ax.set_xlabel('Data')
ax.set_ylabel('Values')
ax.set_title('Box Plot')
```
![5-10](https://github.com/Divya110205/EXNO-5-DS/assets/119404855/350f1086-eb5d-4dc4-bb13-b33526264827)

### 3.Violin Plot
```
data = [np.random.normal(loc=0, scale=1, size=100),
        np.random.normal(loc=2, scale=1, size=100),
        np.random.normal(loc=1, scale=2, size=100)]
plt.violinplot(data)
plt.xlabel('Groups')
plt.ylabel('Values')
plt.title('Violin Plot')
plt.xticks([1, 2, 3], ['Group 1', 'Group 2', 'Group 3'])
plt.show()
```

![5-11](https://github.com/Divya110205/EXNO-5-DS/assets/119404855/03740c40-7a6e-4d7c-b6c6-1f2905f036d1)

### 4.Density Chart
```
data = np.random.normal(0, 1, 1000)
plt.hist(data, bins=30, density=True, alpha=0.5)
plt.title('Density Plot Example')
plt.xlabel('Values')
plt.ylabel('Density')
from scipy.stats import gaussian_kde
kde = gaussian_kde(data)
x_vals = np.linspace(min(data), max(data), 1000)
plt.plot(x_vals, kde(x_vals), 'r')
plt.show()
```

![5-12](https://github.com/Divya110205/EXNO-5-DS/assets/119404855/2b218374-d635-4ea6-a5d0-5ffec3052560)

### 5.Pie Chart
```
act=['eat','sleep','work','play']
slices=[3,7,8,6]
color=['r','y','g','b']
plt.pie(slices,labels=act,colors=color,startangle=90,shadow=True,explode=(0.1,0.1,0.1,0.1),radius=1.2,
autopct='%1.1f%%')
plt.legend()
plt.show()
```

![5-13](https://github.com/Divya110205/EXNO-5-DS/assets/119404855/2491c021-1318-4ccb-841a-57586b3fe1b7)

# Result:
  The Data Visualization using matplot python library is implemented successfully.

