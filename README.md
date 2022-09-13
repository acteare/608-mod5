# 608-mod5
## 7.1 - Introduction
- NumpPy: Preferred Python array implementation. 
#### Operations on arrays are up to two orders of magnitude faster than those on lists. 

## 7.2 - Creating arrays from Existing Data
- Array function: Receives as an argument an array or other collection of elements and returns a new array containing the argument's elements. 
- When outputting an array, NumPy separates each value from the next with a comma and a space and right-aligns all the values using the same field width.
- NumPy auto-formats arrays, based on their number of dimensions, aligning the columns within each row. 

## 7.3 - Array Attributes
- Attributes: Enable you to discover information about its structure and contents.
- dtype attribute:Allows you to check the element type
- ndim: Contains an array's number of dimensions
- shape: contains a tuple specifying an array's dimensions
- size: View an array's total number of elements
- itemsize: The number of bytes required to store each element
- flat: interate through a multidimensional array as if it were one-dimensional

## 7.4 - Filling arrays with Specific Values
#### NumPy provides functions zeros,ones, and full for creating arrays containing 0s, 1s or a specififed value, respectively
      - By default, zeros and ones create arrays containing float64 values.
      
## 7.5 - Creating arrays from Ranges
- Arrange function: used to create integer ranges -- similar to using built-in function range. 
- linspace function: Used to produce evenly spaced floating-point ranges
    - First two arguments specify the starting and ending values in the range. 
    - The ending value is included in the array. 
    - The optional keyword argument "num" specifies the number of evenly spaced values to produce. 
- reshape: used to transform the one-dimensional array into a multidimensional array.
    - You can reshape anty array, provided that the new shape has the same number of elements as the original.
    
## 7.6 - List vs Array Performance: Introducing %timeit
- %timeit magic: times the average duration of operations.
- %load: read code into Ipython from a local file or URL
- %save: to save snippets to a file
- %run: to execute a .pu file from IPython
- %precision: to change the default floating-point precision for IPython outputs
- %cd: to change directions without having to exit IPython first
- %edit: to launch an external editor -- handy if you need to modify more complex snippets
- %history: to view a list of all snippets and commands you've executed in the current IPython session.

## 7.7 - Array Operators
- scalar: When one operand is a single value
- Broadcasting: When NumPy performs the element-wise calculations as if the scalar wer an array of the same shape as the other operand, but with the scalar value in all its elements.
    - Can also be applied between arrays of different sizes and shapes, enabling som econcise and powerful maniupulations.
    
## 7.8 - NumPy Calculation Methods
#### By default, the calculation methods ignore the array's shapes and use all the element sin the calculations. 
#### Many calculation methods can be performed on specific array dimensions, known as the array's axes. 

## 7.9 - Universal Functions
- universal functions (ufuncs): perform various element-wise operations. 
- sqrt universal function: Create an array and caculate the square root of its values
- add universal function: add two arrays with the same shape
- multiply universal function: multiply every element by the scalar value

## 7.10 - Indexing and Slicing
#### One-dimensional arrays can be indexed and sliced using the same syntax and techniques we demonstrated in the "Sequences: Lists and Tuples" chapter. 
- To select an element in a two-dimensional array, specify a tuple containing the element's row and column indices in square brackets
- To select a single row, specify only one index in square brackets
- To select multiple sequential rows, use slice notation
- To select multiple non-sequential rows, use a list of row indices

## 7.11 - Views: Shallow COpies
- Shallow views: view objects (introduced in chapter 6)
- array method "view": returns a new array object with a view of the original array object's data. 
    - Changing a value in the original array, changes the value in the view. 
    - Changing a value in the view also changes that value in the original array
#### Slices also create views. 

## 7.12 - Deep Copies
#### When sharing mutable values, sometimes it's necessary to create a deep copy with independent vopies of the original data. 
  - This is especially important in multi-core programming, where separate parts of your program could attempt to modify your data at the same time, possibly corrupting it. 
- array method copy: returns a new array object with a deep copy of the original array object's data. 

## 7.13 - Reshaping and Transposing
- reshape and resize: Both enable your to change an array's dimensions. 
    - Rehsape returns a view. It does not modify the original array
    - Resize modifies the original array's shape. 
- Flatten and ravel: take a multidemnsional array and flatten it into a single dimension
    - Flatten: deep copies the original array's data
    - ravel: produces a view of the original array, which shares the grades array's data
- Transpose: to "flip" the array, so the rows become the columns and the columns become the rows
    - returns a transposed view of the array
    - Transposing does not modify the original array. 
- Horizontal stacking (hstack): Combine more columns by passing the tuple containing the arrays to combine. 
- Vertical stacking (Vstack): Combine more rows by passing the tuple containing the arrays to combine. 

## 7.14 (Project found in project file)
- Series: an enhanced one-dimensional array
- describe method: produces stats like count, mean, minimum, quartiles, max, etc...
- Interquartile range: the 75% quartile minus the 25% quartile, which is another measure of dispersion, like standard deviation and variance. 
- DataFrame: an enhanced two-dimensional array. 

## 8.1 - Introduction

## 8.2 - Formatting Strings
- d presentation types: format integer values as strings
- c presentation type: formats an integer character code as the corresponding character
- s presentation type: the default. 
- Exponential notation: Can be used to format the values more compactly.

## 8.3 - Concatenating and Repeating Strings
#### Strings are immutable, so each operation assigns a new string object to the variable. 

## 8.4 - Stripping Whitespace from Strings
- strip: removes the leading and trailing whitespace from a string
- lstrip: removes only leading whitespace
- rspace: removes only trailing whitespace

## 8.5 - Changing Character Case
- capitalize: Copies the original string and returns a new string with only the first letter capitalized
- title: copies the original string and returns a new string with only the first character of each work capitalized

## 8.6 - Comparison Operators for Strings
#### Strings may be compared with the comparison operators. 
- Uppercase letters compare as less than lowercase letters because uppercase letters have lower integer values. 

## 8.7 - Searching for Substrings
- count: returns the number of times its argument occurs in the string on which the method is called. 
- index: searches for a substring within a string and returns the first index at which the substring is found. 
    - If it is not found, you will get a ValueError
- rindex: performs the same operation as index, but searches from the end of the string and returns the last index at which the substring is found
- find and rfind: perform the same tasks as index and rindex, but if the substring is not found, it returns an "-1", not a ValueError
- startswith and endswith: return True if the string starts with or ends with a specified substring

## 8.8 - Replacing Substrings
- replace: Takes two substrings. It searches a string for the substring in its first argument and replaces each occurance with the substring in its second argument. The method returns a new string containing the results. 
    - This can receive an optional third argument specifying the maximum number of replacements to perform
    
## 8.9 - Splitting and Joining Strings
- tokens: breaking things into individual componenets such as keywords, identifiers, operators, and other elements of the programming language. 
- delimiters: separate tokens by whitespace characters such as blank, tab and newline, though othe characters may be used. 
- rsplit: performs the same task as split but processes the maximum number of splits from the end of the string toward the beginning
- join: concatenates the string in its argument, which must be an iterable containing only sring values; otherwise, a TypeError occurs. 
- partition: Splits a string into a tuple of three strings based on the method's separator argument
    - The part of the original string before the separator
    - the separator itself, and
    - the part of the string after the separator
- rpartition: Search for the separator from the end of the string
- splitlines: returns a list of new strings representing the lines of text split at eachnewling character in the original string. 

## 8.10 - Characters and Character-Testing Methods
- Characters: the fundamental building blocks of programs
- isdigit: returns true if the string on which you call the method contains only the digit characters
- isalnum: returns true if the string on which you call the method is alphanumeric -- contains only digits and letters

## 8.11 - Raw Strings
- raw strings: treat each backslash as a regular character, rather than the beginning of an escape sequence

## 8.12 - Introduction to Regular Expressions
- regular expressions: describes a search pattern for matching characters in other strings
- re module: allows you to use regular expressions
- fullmatch: checks whether the entire string in its second argument matches the pattern in its first argument
- ? quantifier: matches zero or one occurrences of a subexpression
- sub function: replaces all occurrences of a pettern with the replacement text you specify. 
- split function: tokenizes a string, using a regular expression to specify the delimiter and returns a list of strings
- search function: looks in a string for the first occurrence of a substring that matches a regular expression and returns a match object that contains the matching substring
- ^ metacharacter: (at the beginning) an anchor indicating that the expression matches only the beginning of a string
- $ metacharacter: (at the end) an anchor indicating that the exprssion matches only the end of a string
- findall: finds every matching substring in a string and returns a list of the matching substrings
- finditer_: works like findall but returns a lazy iterable of match objects. 
- () metacharacters: Used to capture substrings in a match. 

## 8.13 - Intro to Data Science: Pandas, Regular Expressions and Data Munging
- Data munging / data wrangling: Preparing data for analysis
#### Two of the most important steps in data munging are data cleaning and transforming data into the optimal formats for your database systems and analytics software. 
    - deleting observations with missing values
    - substituting reasonable values for missing values
    - deleting observations with bad values
    - tossing outliers (although, sometimes you'll want to keep them)
    - duplicate elimination (although sometimes duplicates are valid)
    - dealing with inconsistent data
