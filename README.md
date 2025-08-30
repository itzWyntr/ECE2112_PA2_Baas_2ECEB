# Programming Assignment 2

Objectives: 

1. To identify the codes and functions incorporated in the Numpy library
2. To be able to apply and use the different codes and functions in creating a Python program using a
Numpy library

## Table of Contents

NORMALIZATION PROBLEM: https://github.com/itzWyntr/ECE2112_PA2_Baas_2ECEB/edit/main/README.md#normalization-problem
DIVISIBLE BY 3 PROBLEM: https://github.com/itzWyntr/ECE2112_PA2_Baas_2ECEB/edit/main/README.md#divisible-by-3-problem

### Normalization Problem

In this project, we are asked to normalize a 5x5 array with random numbers

1. Called the Numpy Library
``` python
import numpy as np
```

2. Generated random numbers from 1 to 100 in a 5x5 array

```python
X = np.random.randint(1,101,size=(5,5)) #to give random numbers
print (X)
```

3. Saved the array as "X_normalized.npy"

```python
np.save("X_normalized.npy", X) #to save the array as "X_normalized.npy"
```

4. Called the array

 ```python
original_arr = np.load('X_normalized.npy')
```

5. Used the formula to normalize the array

 ```python
X_normalized = (X-X.mean())/X.std() #to normalize
```
6. Print Results

 ```python
print("The original Array is: \n", original_arr)
print("The normalized Array is: \n",X_normalized)
```

### Divisible by 3 Problem

In this project, we are tasked to create a 10x10 array containing the first 100 square numbers and check which numbers are divisible by 3

1. Called the Numpy Library
``` python
import numpy as np
```
2. Made a list of the first 100 square numbers

``` python
square_list = []

for i in range (1,101):
    square_list.append(i**2) #List all the first 100 square numbers
```

3. Converted the list into an array
``` python
square_arr = np.array(square_list).reshape(10,10) #Converts the list into an array
print("The first 100 square numbers are: \n", square_arr)
```

4. Check if there are numbers divisible by 3 and list them
``` python
divisible_by_3 = square_arr % 3 == 0 #Check if these numbers are divisible by 3
numbers_divisible_by_3 = square_arr[divisible_by_3] #List the numbers that are divisible by 3
```

5. Save the numbers in "div_by_3.npy"
``` python
np.save("div_by_3.npy", numbers_divisible_by_3) #Save the numbers as "div_by_3.npy"
```

6. Load and print the saved numbers
```python
Num_div_by_3 = np.load("div_by_3.npy") #To call "div_by_3.npy" 
print("The numbers divisible by 3 are: \n", Num_div_by_3)
```



   

