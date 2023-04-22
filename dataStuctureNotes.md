## Matrices and List Comprehension

#### What is a matrix?
- representation of data in a 2 dimensional array
- is represented in python as a list within a list
- a matrix has m rows and n columns
- individual pieces of data at row m column n can be called using ```matrix[m][n]  
- code example:

```python
# Python 3 Representation of matrix A

matrix_A = [
    [1, 2, 3, 4],
    [5, 6, 7, 8]
]

# Accessing Matrix A
print('Row 1: %s' % matrix_A[0]) # Recall: Indexing starts at zero in Python
print('Value at Row 2 Column 2: %s' % matrix_A[1][1])
```

Matrices have rules:
- All rows must have the same number of values
- All columns must have the same number of values
- All items in the 2D List must have the same data types
- Since indexing always starts at 0 ... row 1 is technically located at matrix_A[0]

#### What is list comprehension
- concise method to create a list in python 3
It is used when:
- list is made from another iterable
- list is member of another list/sequence/iterable data that satisfies a certain condition
```python
# Old Method
squares = []
for i in range(10):
    squares.append(i ** 2)

print('Our result: %s' % squares)

# List Comprehension

squares = [i**2 for i in range(10)]

print('Our new result: %s' % squares)
```
---

## Map and Filter

#### Map function
- apply a function to an iterable set of data
- returns python iterable data of all the items in the set with the function applied
- can be typcasted into a list
```python
# Example
def square(num):
    ''' squares the given num argument '''
    return num ** 2
# end of square

array = list(range(1,11))
square_array = list(map(square, array))

print('Original Array:', array)
print('Array Squared:', square_array)
```
```
Original Array: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
Array Squared: [1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
```

#### Filter function
- Performs a boolean function (a function that returns true or false) on a data set
- returns python iterable data of all the items that caused the function to return true
Usage:
```filter(function, dataSet)```
- function return true or false, and should also be able to handle the items in the data set as arguments
```python
# Example 3

def isOdd(x):
    ''' isOdd() returns True if x is odd.'''
    return x % 2 != 0

array = list(range(1,101))
odds = list(filter(isOdd, array))

print('Odd Numbers from 1 to 100:', odds)
```
