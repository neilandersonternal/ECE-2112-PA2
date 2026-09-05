# ** ECE-2112-PA2 **

**This is made by Neil Anderson D. Ternal from 2ECE-D**

This is mainly for the content of the repository that I've submitted which covers the three Python problems from our assignment from the course
ECE 2112(Advanced Computer Programming). In which includes Base Computing using Python as a language.

# **A. REPRODUCIBLE NORMALIZATION PROBLEM**

**Objective:**
Create a reproducible random 5 × 5 integer ndarray named X. 
Normalize the complete array using:

Z = X − ¯x/σ 

where ¯x is the mean of all 25 elements and σ is their population standard deviation as returned by
NumPy’s default std() call. Store the normalized array in X normalized.

**Required checks:** Display X, X normalized, its mean, and its standard deviation. Up to floating-
point rounding, the normalized mean must be 0 and the normalized standard deviation must be 1.
The functions that are used in this problem are:

● ```np.random.randomint()``` - used to generate random integers from a discrete uniform distribution within a specified half-open interval.


● ``` size()``` - this is an attribute to an array, and it returns the total number 
of elements across all dimensions.

This attribute of an array made the 5x5 array size possible.

```python
x = np.random.randint(10, 101, size=(5, 5))

print ("Original Array (x):", x)
```

● ```mean()``` - This function computes for the arithmetic mean of a dataset. This function from numpy typical uses for larger arrays/matrices.

This function made the computation of a large arrays instantly computed.


● ```std()``` - This function gets the standard deviation of the Multi-dimensional numerical arrays / matrices.

These functions are all used and contribute to each other in order to solve the problem.
```python
 X_normalized = (x- X_mean)/X_std

print ("X_normalized mean:", X_normalized.mean())
print ("X_normalized standard deviation:", X_normalized.std())

```

# **B. CUBES DIVISIBLE BY 4 PROBLEM**

**Objective:**
Using NumPy, create the first 100 positive integers, cube every element, and reshape the result into a
10 × 10 ndarray named C. Thus, C begins with 13 and ends with 1003.

Use a Boolean condition on C to obtain every cubed value divisible by 4. Store the selected values in
div by 4. Preserve NumPy’s normal row-major selection order.

**Required checks:** Display the shape of C, the array div by 4, and the number of selected elements.
A correct solution has 50 selected elements; the first is 8 and the last is 1,000,000.

The functions that are important in this porblem are:

● ```np.arange()``` - is a core NumPy function used to create a 1D array of evenly spaced values within a given interval
This function is mainly used to create the 1-100 array.

```python
c = (np.arange(1, 101)**3).reshape(10,10)
```

● ```reshape()``` - this function allows you to change the dimensions of an array without altering its underlying data.
This function organizes the dimensions of the array that's created without changing any elements inside. For this case, this was used
to structure the data or else it would look like a one column data.


● ```% (modulo)``` -  calculates the remainder of a division operation. 
This modulo operator is used to calculate the remainder of c divided by 4. Whereas if c is divisible by 4,
the remainder is 0. That's why this was used to narrow down the array into elements that are divisible by 4.

```python
div_by_4 = c[c % 4 == 0]

print ("Shape of C:", c.shape)
print ("Array div_by_4:", div_by_4)
print ("Number of selected elements:", len(div_by_4))
```

( ```len()``` is used to count all the data/elements that are inside the array)
That's all for this problem.


# **C. ABOVE-MEAN SQUARES PROBLEM**

**Objectives:**
Create a 6 × 6 ndarray named S containing the squares of the first 36 positive integers in increasing
row-major order. Compute the mean of all elements of S and store it in S mean. Then use Boolean
filtering to select only the elements strictly greater than S mean. Store these values in above mean.

**Required checks:** Display S, S mean, above mean, and the number of selected elements. A correct
solution has 15 selected elements; the first is 484 and the last is 1296.


● ```np.arange()``` - is a core NumPy function used to create a 1D array of evenly spaced values within a given interval
This was also used in the problem B, but in this case, ```reshape()``` was added in order to make the array look like a 6 x 6 array.

● ```mean()``` - This function computes for the arithmetic mean of a dataset. This function from numpy typical uses for larger arrays/matrices.
This function was used in getting the mean for the 6 x 6 array.


● ```S[S > S_mean]``` - This is made in order to filter the structure of the datas inside the array by getting the datas inside the array "S"
that are greater than the overall mean of the 6 x 6 array.


● ```len()``` -  This function counts the data inside the array. Wherein in this case, was used to count the overall narrowed-data from the
"S[S > S_mean]" equation.

```python
print ("S:", S)
print ("S_mean:", S_mean)
print ("S above mean:", above_mean)
print ("Number of selected elements:", len(above_mean))
```
That's all for my second assignment. Thank you for reading!!

**README** file version history:

August 30, 2026: Initial README output uploaded.

September 5, 2026:  python code example was enhanced.










