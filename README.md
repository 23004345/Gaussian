# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1.importing numpy function
2.use numpy and sys packages
3.use nested loops to loop through each row and column 
4.end the program

## Program:
```
/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by:Devesh s 
RegisterNumber:23004345 
*/
```

import numpy as np

import sys

n=int(input())

a=np.zeros((n,n+1))

x=np.zeros(n)

for i in range(n):

    for j in range(n+1):
    
        a[i][j] = float(input())
        
for i in range(n):

    if a[i][i]==0.0:
    
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

    print('X%d = %0.2f' %(i,x[i]), end = ' ')
    
        
            

## Output:![Screenshot 2023-12-31 131612](https://github.com/23004345/Gaussian/assets/138849203/c87b1c87-7dda-4c85-82c3-92f80efcdd95)

![gaussian elimination]()


## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

