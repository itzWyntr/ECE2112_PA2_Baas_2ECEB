# Programming Assignment 2

Objectives: 

1. To identify the codes and functions incorporated in the Numpy library
2. To be able to apply and use the different codes and functions in creating a Python program using a
Numpy library

##Table of Contents

NORMALIZATION PROBLEM: 
DIVISIBLE BY 3 PROBLEM:

### Normalization Problem

In this project, we are asked to normalize a 5x5 array with random numbers

1. I called the Numpy Library
``` python
import numpy as np
```

2. Then generated random numbers from 1 to 100 in a 5x5 array

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




