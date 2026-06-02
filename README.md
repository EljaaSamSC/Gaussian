# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. 
2. 
3. 
4. 

## Program:
```
#Program to solve a matrix using Gaussian elimination without partial pivoting.
#Developed by: Eljaa Sam S C
#RegisterNumber: 212225040085
import os
os.environ['OPENBLAS_NUM_THREADS']="1"
import numpy as np
import sys
n=int(input())
a=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        a[i][j]=float(input())
for i in range(n):
    if a[i][i]==0:
        sys.exit('Divide by zero detected!')
    for j in range(i+1,n):
        ratio=a[j][i]/a[i][i]
        for k in range(n+1):
           a[j][k]=a[j][k]-ratio*a[i][k]
x[n-1]=a[n-1][n]/a[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]=a[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-a[i][j]*x[j]
    x[i]=x[i]/a[i][i]
for i in range(n):
    print('X%d = %0.2f' % (i,x[i]),end=' ')
```

## Output:

<img width="1209" height="562" alt="{84410448-5830-4C6B-94DD-42FE9B43F938}" src="https://github.com/user-attachments/assets/7b79428e-cd6a-4a71-8d77-1bb059c45933" />


## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

