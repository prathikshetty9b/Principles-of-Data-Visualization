# Principles of Data Visualization

## Assignment 1 | Due Date : 23 Nov 2021

## NumPy Exercises

1.  Create a 4x2 integer array and print it's attributes
2.  Create a 5x2 integer array from a range between 100 to 200 such that the difference between 
each element is 10.
3.  Return array of odd rows and even columns from Numpy array of your choice.
4.  Create a result array by adding the following two NumPy arrays. Next, modify the result array by 
calculating the square of each element.
5.  Split the array into four equal sized sub arrays.
6.  Print max from axis 0 and min from axis 1 from the 2-D array of your choice.
7.  Delete the second column from a given array and insert the new column in its place.

### 1.  Create a 4x2 integer array and print it's attributes


```python
#import numpy
import numpy as np

#Create 4x2 Numpy array
array = np.array([1,2,3,4,5,6,7,8])

array = array.reshape(4,2)

array
```




    array([[1, 2],
           [3, 4],
           [5, 6],
           [7, 8]])




```python
#dimension of array 
array.ndim
```




    2




```python
#array shape
array.shape
```




    (4, 2)




```python
#Datatype of variables inside array
array.dtype
```




    dtype('int32')




```python
#Array type
type(array)
```




    numpy.ndarray



### Create a 5x2 integer array from a range between 100 to 200 such that the difference between each element is 10.


```python
#Create an 5x2 array
array1 = np.arange(100,200,10).reshape(5,2)

#print
array1
```




    array([[100, 110],
           [120, 130],
           [140, 150],
           [160, 170],
           [180, 190]])



### 3.  Return array of odd rows and even columns from Numpy array of your choice.


```python
# Create an array using arange
array2 = np.arange(1,21).reshape(5,4)

array2

```




    array([[ 1,  2,  3,  4],
           [ 5,  6,  7,  8],
           [ 9, 10, 11, 12],
           [13, 14, 15, 16],
           [17, 18, 19, 20]])




```python
#Select odd rows and even columns
array2[::2,1::2]
```




    array([[ 2,  4],
           [10, 12],
           [18, 20]])



### 4.  Create a result array by adding the following two NumPy arrays. Next, modify the result array by calculating the square of each element.


```python
# Create two arrays 
arrayA = np.arange(1,5).reshape(2,2)
arrayB = np.arange(5,9).reshape(2,2)

#Sum
resultArray = arrayA +arrayB
resultArray


```




    array([[ 36,  64],
           [100, 144]], dtype=int32)




```python
#Square
np.square(resultArray)
```




    array([[ 36,  64],
           [100, 144]], dtype=int32)



### 5.  Split the array into four equal sized sub arrays.


```python
#split array  into 4 equal parts
array = np.arange(12).reshape(4,3)
np.split(array,4)
```




    [array([[0, 1, 2]]),
     array([[3, 4, 5]]),
     array([[6, 7, 8]]),
     array([[ 9, 10, 11]])]



### 6.  Print max from axis 0 and min from axis 1 from the 2-D array of your choice.


```python
#Create array
array = np.arange(12).reshape(4,3)

#max in each column
np.amax(array,0)
```




    array([ 9, 10, 11])




```python
#max in each column
np.amax(array,1)
```




    array([ 2,  5,  8, 11])




```python
#min in each column
np.amin(array,0)
```




    array([0, 1, 2])




```python
#min in each row
np.amin(array,1)
```




    array([0, 3, 6, 9])





### 7.  Delete the second column from a given array and insert the new column in its place.


```python
#Create array 
array = np.arange(12).reshape(4,3)
array
```




    array([[ 0,  1,  2],
           [ 3,  4,  5],
           [ 6,  7,  8],
           [ 9, 10, 11]])




```python
#Delete Second Column
arrayDel = np.delete(arrayDel,1,axis=1)
arrayDel
```




    array([[ 0,  2],
           [ 3,  5],
           [ 6,  8],
           [ 9, 11]])




```python
#Insert to Second Column
ins = [1,2,3,4]
arrayInsert = np.insert(arrayDel,1,ins,axis=1)
arrayInsert
```




    array([[ 0,  1,  2],
           [ 3,  2,  5],
           [ 6,  3,  8],
           [ 9,  4, 11]])


