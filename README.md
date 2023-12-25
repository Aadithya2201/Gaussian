# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. Import the numpy module and sys module to use the built-in functions for calculation 2. Get the size of the matrix from user and create empty matrix and vector
3. using for loop get elements for matrix and vector
4. Using another for loop to take each element in the matrix
5. solve row echelon form
6. perform back substitution
7. print the value in two decimal points 8. End the program

## Program:
```
'''Program to solve a matrix using Gaussian elimination without partial pivoting.
Developed by: Aadithya.R
RegisterNumber: 23006361
'''
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
        sys.exit('Divide by zero detected:')
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
    print('X%d = %0.2f'%(i,x[i]),end=' ')
        

```

## Output:
![Screenshot 2023-12-25 134050](https://github.com/Aadithya2201/Gaussian/assets/145917810/c3e14287-1a0f-498b-bf83-6a9158d7a828)
![Screenshot 2023-12-25 134119](https://github.com/Aadithya2201/Gaussian/assets/145917810/20d024b7-ecc9-4d94-8aa5-41dbcdbbf1c7)



## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

