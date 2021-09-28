# String and Variables 

## String :
* In Python, Strings are arrays of bytes representing Unicode characters
* Square brackets can be used to access elements of the string

## String with the use of Single Quotes: 
```
String1 = 'Welcome to the Geeks World'
print("String with the use of Single Quotes: ")
print(String1)


Welcome to the Geeks World

```

## String with the use of Double Quotes: 
```
String1 = "I'm a Geek"
print("\nString with the use of Double Quotes: ")
print(String1)

I'm a Geek
```
## String with the use of Triple Quotes: 
```
String1 = '''Geeks
            For
            Life'''
print("\nCreating a multiline String: ")
print(String1)

I'm a Geek and I live in a world of "Geeks"

```

# Variables:
* Variables are containers for storing data values
* Python has no command for declaring a variable

## Casting 
```if you want to specify the data type of a variable, this can be done with casting```
```
x = str(3)    # x will be '3'
y = int(3)    # y will be 3
z = float(3)  # z will be 3.0

print(x)
print(y)
print(z)
```
# Types of Variables:
* Variable Names
* Assign Multiple Values
* Output Variables
* Global Variables

## Variable Names:
#### A variable can have a short name (like x and y) or a more descriptive name (age, carname, total_volume). Rules for Python variables:
* A variable name must start with a letter or the underscore character
* A variable name cannot start with a number
* A variable name can only contain alpha-numeric characters and underscores (A-z, 0-9, and _ )
* Variable names are case-sensitive (age, Age and AGE are three different variables)

```
Legal variable names:

myvar = "John"
my_var = "John"
_my_var = "John"
myVar = "John"
MYVAR = "John"
myvar2 = "John"

Illegal variable names:

2myvar = "John"
my-var = "John"
my var = "John"

```

## Multi Words Variable Names
```
Variable names with more than one word can be difficult to read.

There are several techniques you can use to make them more readable:

Camel Case
Each word, except the first, starts with a capital letter:
    myVariableName = "John"

Pascal Case
Each word starts with a capital letter:
    MyVariableName = "John"

Snake Case
Each word is separated by an underscore character:
    my_variable_name = "John"

```

## Assign Multiple ValuesAssign Multiple Values

### Python allows you to assign values to multiple variables in one line:
```
Many Values to Multiple Variables:
    x, y, z = "dev", "test", "Prod"
    print(x, y, z)

One Value to Multiple Variables:
    x = y = z = "Orange"

Unpack a list:
    fruits = ["apple", "banana", "cherry"]
    x, y, z = fruits
    print(x)
    print(y)
    print(z)
```

## Output Variables
### The Python print statement is often used to output variables.
```
To combine both text and a variable, Python uses the + character:
    x = "awesome"
    print("Python is " + x)

You can also use the + character to add a variable to another variable:
    x = "Python is "
    y = "awesome"
    z =  x + y
    print(z)

For numbers, the + character works as a mathematical operator:
    x = 5
    y = 10
    print(x + y)

If you try to combine a string and a number, Python will give you an error:
    x = 5
    y = "John"
    print(x + y)

```

# Global Variables:
## Variables that are created outside of a function (as in all of the examples above) are known as global variables.
## Global variables can be used by everyone, both inside of functions and outside.

### Create a variable outside of a function, and use it inside the function
```
Example 1

    x = "awesome"

    def myfunc():
    print("Python is " + x)

    myfunc()
    
Python is awesome
```
### If you create a variable with the same name inside a function, this variable will be local, and can only be used inside the function. The global variable with the same name will remain as it was, global and with the original value.
```
Example 2 
    x = "awesome"

    def myfunc():
    x = "fantastic"
    print("Python is " + x)

    myfunc()


    print("Python is " + x)

Python is fantastic
Python is awesome
```
# global Keyword

### Normally, when you create a variable inside a function, that variable is local, and can only be used inside that function.
### To create a global variable inside a function, you can use the global keyword.
### If you use the global keyword, the variable belongs to the global scope:
```
    def myfunc():
    global x
    x = "fantastic"

    myfunc()

    print("Python is " + x)

Python is fantastic
```
### To change the value of a global variable inside a function, refer to the variable by using the global keyword:
```
    x = "awesome"

    def myfunc():
    global x
    x = "fantastic"

    myfunc()

    print("Python is " + x)

Python is fantastic
```