# Python Cheatsheet

## Main
```python
if __name__ == '__main__':    # If file is not imported, this will be executed
    main()
```

## Basic and necessary commands needed to execute a well-defined python code at the command line.

### Opening a python shell.
```python
$ python3               
```

### Installing a package
```python
$ pip3 install <package-name>              
```

### Running a python script
```python
$ python3 <filename>.py                   
```

### Calculating the time of execution
```python 
$ time python3 <filename>.py                  
```

### Importing a py script
```python
import <filename>.py
```

## Getting started with the language

### Basic I/O
+ Input
```python
input("Input: ")

```
+ Python always take inputs as a string.
If you want to take a decimal number (Int, Float,etc). Use typecasting
```python
int(input("Input: "))

```
+ Output
Python automatically points the cursor to a new line.
We need not specify explicitly.
```python
print("Output")
```

### Variables and Constants
In python, we need not specify the datatype of a variable. 
The interpreter interprets the value and assigns a suitabe datatype for that.
```python
number = 0
org = "GitHub"
```

### Conditional Statements
In python, we do not write a block of code in a pair of paranthesis.
We write it after `:` followed by an indentation in the next line.

The conditional statements include `if`, `if-elif-else`, `if-else`, `nested if` and so on... (elif = else if)
```python
x,y = 0,1
if x < y:
  print("x is less than y)
elif x > y:
  print("x is not less than y")
else:
  print("x is equal to y")
```
Note that the colon (:) following <expr> is required.
Similarly, the `nested if` also works.


### Iterative statements
As other programming languages, we have 

+ `for loop`
```python
for i in range(5):
  print(i)
```

+ `for loop iterating over characters in string or values of list`
```python
for char in <string>:
  print(char, end="")                     # end argument for not changing to next line by default
 or
for item in <list>:
  print(item)                            # print each elements of the list on different line

 
The `range` function starts off with 0 till the number(excluded). The `range` function can be initialised at any number i = 1, 2, etc.. Just change the range(i,n) till 1 less then `n`. You caneven change the iteration value by specifying the key (k), by default k is 1 if not specified. For example.. range(i,n,k) the range will increment i value by adding k to the i.

+ `while loop`
```python
i=0
while(i < 10):
  print("{} is less than 10".format(i))
  i += 1
```
`.format()` is a type of printing.

## Data Structures

### Lists
```python
# These are all inplace operations returns a None value
<list_name> = [] or list()      # Create an empty list

<list>.append(<ele>)            # Add an element to the end of the list
<list>.sort()                   # Sorts the same given list
sorted(<list>)                  # If don't want to sort the original list.
<list>.pop([<ele>])             # Removes the last element if no argument else removes the element at the index given
<list>.clear()                  # Makes it an empty list
<list>.insert(<index>, <ele>)   # Adds the element at the index
<list>.extend(<iterator>)
<list>.reverse()                # Reverse a given list
<list>.clear()                  # Clears all the elements present in list
```

```python
# These are not inplace operations and has a return value

<list>.copy()                   # Makes a shallow copy of the list
<list>.index(<ele>)             # Returns the index of the given element
<list>.count(<ele>)             # Returns the number of occurrences of the element
```
### Dictionaries
key-value pairs.
```python
<dict_name> = {} or dict()                                # Creating an empty dictionary
<dict> = {'Google':100, 'Facebook':80, 'Apple':90}
# key ca be a decimal number and values can be anything from a string, decimal number to list or a dictionary itself.

<dict>['Amazon'] = 85                           # Adding a key along with the value

# Accessing the dictionary 
for key in <dict>:
  print("{key} -> {x}".format(key=key, x=<dict>[key]))

# Accessing both the key and value in the dictionary
for key, value in <dict>.items():
    print("{} -> {}".format(key, value))
 
<dict>.keys()                                   # Return a sequence of all the keys present in Dictionary / Print all the keys
<dict>.values()                                 # Return a sequence of all the values present in Dictionary / Print all the values
len(<dict>)                                     # Find the length of the dictionary
<dict>.pop(<key>)                               # Removes the item with the specified key name
del <dict>[<key>]                               # delete the item
<dict>.copy()                                   # Make a copy of a dictionary
<dict>.clear()                                  # Clears all the keys and values stored in dictionary
<dict>.update(<other_dict>)                     # Combine 2 dictionaries. If same key is present in both the dictionaries then the value of the first dictionary will be replaced                                                 # by other_dictionary value coresponding to the key.
```
A dictionary can also contain many dictionaries, this is called nested dictionaries.

## Third party libraries

### Pandas
```shell
$ sudo pip3 install pandas          # Installing pandas module in Ubuntu
```
```python
import pandas as pd

<dataframe>.head([<n>])             # Display the first n rows of the Dataframe, default value is 5 rows
<dataframe>.tail([<n>])             # Display the last n rows of the Dataframe, default value is 5 rows
<dataframe>.info()                  # Gives some information like, row and column datatypes, non-null count, and memory usage
<dataframe>.describe()              # Provides some descriptive statistics about the numerical rows in the dataframe
```
### NLTK
```shell
$ sudo pip3 install nltk                    # Installing nltk module in Ubuntu
```
```python
import nltk

# Before trying any function download the word list
nltk.download('punkt')
nltk.download('averaged_perceptron_tagger')
```

# Can install many libraries present on pypi.org example- numpy, matplotlib, sklearn, tensorflow, etc.. These are all Data science related libraries/Packages. 
