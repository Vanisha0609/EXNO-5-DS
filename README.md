# EXNO-5-DS-DATA VISUALIZATION USING MATPLOT LIBRARY

# Aim:
  To Perform Data Visualization using matplot python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:
 TO CAPTURE A TREND
 
  1.LINE CHART
 ```
import matplotlib.pyplot as plt
import numpy as np
x=[0,1,2,3,4,5]
y=[0,1,4,9,16,25]
plt.plot(x,y,color='plum')
plt.show()
```
![image](https://github.com/Vanisha0609/EXNO-5-DS/assets/119104009/30512fa0-5a47-4be7-b6ef-b7444b2ab721)
2.MULTI-LINE CHART
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
![image](https://github.com/Vanisha0609/EXNO-5-DS/assets/119104009/d76efe55-7d99-4a89-9dcc-9ff09abfc4ea)

3.AREA CHART
```
x=[1,2,3,4,5]
y1=[10,12,14,16,18]
y2=[5,7,9,11,13]
y3=[2,4,6,8,10]
plt.fill_between(x,y1,color='thistle')
plt.fill_between(x,y2,color='lightblue')
plt.plot(x,y1,color='red')
plt.plot(x,y2,color='teal')
plt.legend(['y1','y2'])
plt.show()
```
![image](https://github.com/Vanisha0609/EXNO-5-DS/assets/119104009/40cc251e-173c-48c0-a578-baff9ffca170)

4. STACKED AREA CHART
```
plt.stackplot(x,y1,y2,y3,labels=['Line 1','Line 2','Line 3'])
plt.legend(loc='upper left')
plt.title('Stacked Line Chart')
plt.xlabel('X-axis')
plt.ylabel('Y-axis')
plt.show()
```
![image](https://github.com/Vanisha0609/EXNO-5-DS/assets/119104009/f00d46fd-6a5b-4844-9974-399e136e2fd2)

5.SPLINE CHART
```
from scipy.interpolate import make_interp_spline
x=np.array([1,2,3,4,5,6,7,8,9,10])
y=np.array([2,4,5,7,8,8,9,10,11,12])
spl=make_interp_spline(x,y)
x1=np.linspace(x.min(),x.max(),100)
y1=spl(x1)
plt.plot(x,y,'*',label='data',color='slategrey')
plt.plot(x1,y1,'-',label="spline",color='plum')
plt.legend()
plt.show()
```
![image](https://github.com/Vanisha0609/EXNO-5-DS/assets/119104009/f5193e1a-4333-4ed6-919b-53e0caf948b7)

TO VISUALIZE RELATIONSHIPS

1. BAR CHART
```
val=[5,6,3,7,2]
names=["A","B","C","D","E"]
plt.bar(names,val,color="mediumaquamarine")
plt.show()
```
![image](https://github.com/Vanisha0609/EXNO-5-DS/assets/119104009/c82ec0a1-2c9b-4b86-a9fa-ec073a8e091c)

2.SCATTER PLOT

```
x=[0,1,2,3,4,5]
y=[0,1,4,9,16,25]
plt.scatter(x,y,s=30,color="cadetblue")
plt.show()
```
![image](https://github.com/Vanisha0609/EXNO-5-DS/assets/119104009/75dc2825-aa4e-4d18-9e50-6580526d0a45)

3.BUBBLE CHART

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
![image](https://github.com/Vanisha0609/EXNO-5-DS/assets/119104009/140c55fc-0828-4558-a1a1-22daf4dd3647)

TO CAPTURE DISTRIBUTIONS
1. HISTOGRAM

```
ages=[2,5,70,40,30,45,50,45,43,40,44,60,7,13,57,18,90,77,32,21,20,40]
range=(0,100)
bins=10
plt.hist(ages,bins,range,color='cornflowerblue',histtype='bar',rwidth=0.8)
plt.xlabel('age')
plt.ylabel('No. Of People')
plt.title('Histogram')
plt.show()
```
![image](https://github.com/Vanisha0609/EXNO-5-DS/assets/119104009/98b8a8c5-7fa9-4563-8ac4-b430ff830fd4)

2.BOX PLOT
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
![image](https://github.com/Vanisha0609/EXNO-5-DS/assets/119104009/5893206f-36fd-422a-97f2-fa321a8f8abe)

3.VIOLIN PLOT

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
![image](https://github.com/Vanisha0609/EXNO-5-DS/assets/119104009/ac0a7888-4cdf-4a73-beb5-9198a03fb831)

4.DENSITY CHART

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
![image](https://github.com/Vanisha0609/EXNO-5-DS/assets/119104009/afb3d4c5-53fd-4ac1-a75c-d124d818b421)

5.PIE CHART
```
act=['eat','sleep','work','play']
slices=[3,7,8,6]
color=['coral','lightsteelblue','lavender','darkkhaki']
plt.pie(slices,labels=act,colors=color,startangle=90,shadow=True,explode=(0.1,0.1,0.1,0.1),radius=1.2,
autopct='%1.1f%%')
plt.legend()
plt.show()
```
<img src="https://github.com/Vanisha0609/EXNO-5-DS/assets/119104009/28f1a6b7-02fc-4152-89bb-050084cc4058" width="100" height="100">

# Result:
 The Data Visualization using matplot python library is implemented successfully.
