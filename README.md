# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. import numpy
2. import sys
3. solve using loop
4. print the output

## Program:
```
/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: VIDHYA SHREE K
RegisterNumber: 25008027
*/
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
        r=a[j][i]/a[i][i]
        for k in range(n+1):
            a[j][k]=a[j][k]-r*a[i][k]
x[n-1]=a[n-1][n]/a[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]=a[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-a[i][j]*x[j]
    x[i]=x[i]/a[i][i]
for i in range(n):
    print('X%d = %0.2f'%(i,x[i]),end=" ")
```

## Output:
<img width="1920" height="1200" alt="Screenshot 2025-11-27 112344" src="https://github.com/user-attachments/assets/8a1d459d-a055-480b-a84f-429f4c0afc81" />
<img width="1920" height="1200" alt="Screenshot 2025-11-27 112358" src="https://github.com/user-attachments/assets/a352c517-e6eb-4a9b-ba31-1a1d83b2ada0" />



## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

