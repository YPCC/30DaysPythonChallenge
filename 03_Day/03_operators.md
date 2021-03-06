<div align="center">
  <h1> 30 Days Of Python: Day 3 - Operators</h1>
  <a class="header-badge" target="_blank" href="https://www.linkedin.com/in/asabeneh/">
  <img src="https://img.shields.io/badge/style--5eba00.svg?label=LinkedIn&logo=linkedin&style=social">
  </a>
  <a class="header-badge" target="_blank" href="https://twitter.com/Asabeneh">
  <img alt="Twitter Follow" src="https://img.shields.io/twitter/follow/asabeneh?style=social">
  </a>

<sub>Author:
<a href="https://www.linkedin.com/in/asabeneh/" target="_blank">Asabeneh Yetayeh</a><br>
<small> First Edition: Nov 22 - Dec 22, 2019</small>
</sub>

</div>
</div>

[<< Day 2](../02_Day/02_variables.md) | [Day 4 >>](../04_Day/04_string.md)

![30DaysOfPython](../images/30DaysOfPython_banner3@2x.png)

- [📘 Day 3](#%f0%9f%93%98-day-3)
  - [Boolean](#boolean)
  - [Operators:](#operators)
    - [Assignment Operators:](#assignment-operators)
    - [Arithmetic Operators:](#arithmetic-operators)
    - [Comparison Operators](#comparison-operators)
    - [Logical Operators](#logical-operators)
  - [💻 Exercises - Day 3](#%f0%9f%92%bb-exercises---day-3)

# 📘 Day 3

## Boolean

A boolean data type represents one of the two values:_True_ or _False_. The use of these data types will be clear when you start the comparison operator. The first letter **T** for True and **F** for False should be capital unlike JavaScript.
**Example: Boolean Values**

```py
print(True)
print(False)
```

## Operators:

Python language supports several types of operators. In this section, we will focus on few of them.

### Assignment Operators:

Assignment operators are used to assign values to variables. Let's take = as an example. Equal sign in mathematics shows that two values are equal, however in python it means we are storing a value in a certain variable and we call it assignment or a assigning value to a variable. The table below shows the different types of python assignment operators, taken from [w3school](https://www.w3schools.com/python/python_operators.asp).

![Assignment Operators](../images/assignment_operators.png)

### Arithmetic Operators:

- Addition(+): a + b
- Subtraction(-): a -b
- Multiplication(_):a _ b
- Division(/): a / b
- Modulus(%):a % b
- Floor division(//): a // b
- Exponential(**):a ** b

![Arithmetic Operators](../images/arithmetic_operators.png)

**Example:Integers**

```py
# Arithmetic Operations in Python
# Integers

print('Addition: ', 1 + 2)
print('Subtraction: ', 2 - 1)
print('Multiplication: ', 2 * 3)
print ('Division: ', 4 / 2)                         # Division in python gives floating number
print('Division: ', 6 / 2)
print('Division: ', 7 / 2)
print('Division without the remainder: ', 7 // 2)   # gives without the floating number or without the remaining
print('Modulus: ', 3 % 2)                           # Gives the remainder
print ('Division without the remainder: ',7 // 3)
print('Exponential: ', 3 ** 2)                      # it means 3 * 3
```

**Example:Floats**

```py
# Floating numbers
print('Floating Number,PI', 3.14)
print('Floating Number, gravity', 9.81)
```

**Example:Complex numbers**

```py
# Complex numbers
print('Complex number: ', 1+1j)
print('Multiplying complex number: ',(1+1j) * (1-1j))
```

Let's declare a variable and assign a number data type. I am going to use single character variable but remember do not develop a habit of declaring such types of variable. Variable names should be all the time mnemonic.

**Example:**

```python
# Declaring the variable at the top first

a = 3 # a is a variable name and 3 is an integer data type
b = 2 # b is a variable name and 3 is an integer data type

# Arithmetic operations and assigning the result to a variable
total = a + b
diff = a - b
product = a * b
division = a / b
remainder = a % b
floor_division = a // b
exponential = a ** b

# I should have used sum instead of total but sum is a built-in function try to avoid overriding builtin functions
print(total) # if you don't label your print with some string, you never know from where is  the result is coming
print('a + b = ', total)
print('a - b = ', diff)
print('a * b = ', product)
print('a / b = ', division)
print('a % b = ', remainder)
print('a // b = ', floor_division)
print('a ** b = ', exponential)
```

**Example:**

```py
print('== Addition, Subtraction, Multiplication, Division, Modulus ==')

# Declaring values and organizing them together
num_one = 3
num_two = 4

# Arithmetic operations
total = num_one + num_two
diff = num_two - num_one
product = num_one * num_two
div = num_two / num_two
remainder = num_two % num_one

# Printing values with label
print('total: ', total)
print('difference: ', diff)
print('product: ', product)
print('division: ', div)
print('remainder: ', remainder)
```

Let's start start connecting the dots and start making use of what we knew to calculate(area, volume, weight, perimeter, distance, force)

**Example:**

```py
# Calculating area of a circle
radius = 10                                 # radius of a circle
area_of_circle = 3.14 * radius ** 2         # two * sign means exponent or power
print('Area of a circle:', area_of_circle)

# Calculating area of a rectangle
length = 10
width = 20
area_of_rectangle = length * width
print('Area of rectangle:', area_of_width)

# Calculating a weight of an object
mass = 75
gravity = 9.81
weight = mass * gravity
print(weight, 'N')                         # Adding unit to the weight
```

### Comparison Operators

In programming we compare values, we use comparison operators to compare two values. We check if a value is greater or less or equal to other value. The following table shows python comparison operators which was taken from [w3shool](https://www.w3schools.com/python/python_operators.asp).

![Comparison Operators](../images/comparison_operators.png)
**Example: Comparison Operators**

```py
print(3 > 2)     # True, because 3 is greater than 2
print(3 >= 2)    # True, because 3 is greater than 2
print(3 < 2)     # False,  because 3 is greater than 2
print(2 < 3)     # True, because 2 is less than 3
print(2 <= 3)    # True, because 2 is less than 3
print(3 == 2)    # False, because 3 is not equal to 2
print(3 != 2)    # True, because 3 is not equal to 2
print(len('mango') == len('avocado'))  # False
print(len('mango') != len('avocado'))  # True
print(len('mango') < len('avocado'))   # True
print(len('milk') != len('meat'))      # False
print(len('milk') == len('meat'))      # True
print(len('tomato') == len('potato'))  # True
print(len('python') > len('dragon'))   # False


# Comparing something give either a True or False

print('True == True: ', True == True)
print('True == False: ', True == False)
print('False == False:', False == False)
print('True and True: ', True and True)
print('True or False:', True or False)

```

In addition to the above comparison operator python uses:

- _is_: Returns true if both variables are the same object(x is y)
- _is not_: Returns true if both variables are not the same object(x is not y)
- _in_: Returns True if a list with the a certain item(x in y)
- _not in_: Returns True if a list doesn't have the a certain item(x in y)

```py
print('1 is 1', 1 is 1)                   # True - because the data values are the same
print('1 is not 2', 1 is not 2)           # True - because 1 is not 2
print('A in Asabeneh', 'A' in 'Asabeneh') # True - A found in the string
print('B in Asabeneh', 'B' in 'Asabeneh') # False -there is no uppercase B
print('coding' in 'coding for all') # True - because coding for all has the word coding
print('a in an:', 'a' in 'an')      # True
print('4 is 2 ** 2:', 4 is 2 **2)   # True
```

### Logical Operators

Unlike other programming languages python uses the key word _and_, _or_ and _not_ for logical operator. Logical operators are used to combine conditional statements:

![Logical Operators](../images/logical_operators.png)

```py
print(3 > 2 and 4 > 3) # True - because both statements are true
print(3 > 2 and 4 < 3) # False - because the second statement is false
print(3 < 2 and 4 < 3) # False - because both statements are false
print(3 > 2 or 4 > 3)  # True - because both statements are true
print(3 > 2 or 4 < 3)  # True - because one of the statement is true
print(3 < 2 or 4 < 3)  # False - because both statements are false
print(not 3 > 2)     # False - because 3 > 2 is true, then not True gives False
print(not True)      # False - Negation, the not operator turns true to false
print(not False)     # True
print(not not True)  # True
print(not not False) # False
```

🌕 You have boundless energy. You have just completed day 3 challenges and you are three steps a head in to your way to greatness. Now do some exercises for your brain and for your muscle.

## 💻 Exercises - Day 3

1. Declare your age as integer variable
2. Declare your height as a float variable
3. Declare a complex number variable
4. Write a script that prompt the user to enter base and height of the triangle and calculate an area of a triangle (area = 0.5 x b x h).

```py
    Enter base: 20
    Enter height: 10
    The area of the triangle is 50
```

5. Write a script that prompt the user to enter side a, side b, and side c of the triangle and and calculate the perimeter of triangle (perimeter = a + b + c)

```py
Enter side a: 5
Enter side b: 4
Enter side c: 3
The perimeter of the triangle is 12
```

6. Get length and width using prompt and calculate an area of rectangle (area = length x width and the perimeter of rectangle (perimeter = 2 x (length + width))
7. Get radius using prompt and calculate the area of a circle (area = pi x r x r) and circumference of a circle(c = 2 x pi x r) where pi = 3.14.
8. Calculate the slope, x-intercept and y-intercept of y = 2x -2
9. Slope is (m = y2-y1/x2-x1). Find the slope between point (2, 2) and point(6,10)
10. Compare the slope of q10 and 11
11. Calculate the value of y (y = x^2 + 6x + 9). Try to use different x values and figure out at what x value y is 0.
12. Find the length of python and jargon and make a falsy comparison statement.
13. Use _and_ operator to check if 'on' is found in both python and jargon
14. _I hope this course is not full of jargon_. Use _in_ operator to check if _jargon_ is in the sentence.
15. There is no 'on' in both dragon and python
16. Find the length of the text _python_ and convert the value to float and convert it to string
17. Even numbers are divisible by 2 and the remainder is zero. How do you check if a number is even or not using python?
18. The floor division of 7 by 3 is equal to the int converted value of 2.7.
19. Check if type of '10' is equal to 10
20. Check if int('9.8') is equal to 10
21. Writ a script that prompt a user to enters hours and rate per hour. Calculate pay of the person?

```py
Enter hours: 40
Enter rate per hour: 28
Your weekly earning is 1120
```

22. Write a script that prompt the user to enter number of years. Calculate the number of seconds a person can live. Assume some one lives just hundred years

```py
Enter number of yours you live: 100
You lived 3153600000 seconds.
```

23. Write a python script that display the following table

```py
1 1 1 1 1
2 1 2 4 8
3 1 3 9 27
4 1 4 16 64
5 1 5 25 125
```

🎉 CONGRATULATIONS ! 🎉

[<< Day 2](../02_Day/02_variables.md) | [Day 4 >>](../04_Day/04_string.md)
