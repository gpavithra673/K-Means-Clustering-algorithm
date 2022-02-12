# Implementation of K-Means Clustering Algorithm
## Aim
To write a python program to implement K-Means Clustering Algorithm.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation

## Algorithm:

### Step 1:
import the necessary packages.

### Step 2:
Read the csv file.

### Step 3:
Scatter plot the applicant income and loan amount.

### Step 4:
Obtain the kmean clustring for 2 classes.

### Step 5:
Pretict the cluster group of Applicant Income and Loanamount.

## Program:
~~~
#Developed by NAME:G.Pavithra
#Regisno:212221240036
import pandas as pd
import matplotlib.pyplot as plt
from sklearn.cluster import KMeans
import seaborn as sns
import warnings
warnings.filterwarnings('ignore')

x1 = pd.read_csv('clustering.csv')
print(x1.head(2))
x2 = x1.loc[:, ['ApplicantIncome','LoanAmount']]
print(x2.head(2))

x = x2.values
sns.scatterplot(x[:,0], x[:,1])
plt.xlabel('Income')
plt.ylabel('Loan')
plt.show()

kmean =KMeans(n_clusters=3)
kmean.fit(x)

print('Clusters Centers:', kmean.cluster_centers_)
print('Labels:', kmean.labels_)

predicted_class = kmean.predict([[1000,100]])
print('The cluster group for Applicant Income 1000 and Loanamount 100 :' ,predicted_class)
~~~
## Output:

### Insert your output
![output](m4.png)
![output](m5.png)
## Result
Thus the K-means clustering algorithm is implemented and predicted the cluster class using python program.