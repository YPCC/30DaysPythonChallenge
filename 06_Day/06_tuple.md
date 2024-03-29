<div align="center">
  <h1> 30 Days Of Python: Day 6 - Tuple</h1>
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

[<< Day 5](../05_Day/05_list.md) | [Day 7 >>](../07_Day/07_set.md)

![30DaysOfPython](../images/30DaysOfPython_banner3@2x.png)

- [Day 6:](#day-6)
  - [Tuple](#tuple)
    - [Creating Tuple](#creating-tuple)
    - [Tuple length](#tuple-length)
    - [Accessing tuple items](#accessing-tuple-items)
    - [Slicing tuples](#slicing-tuples)
    - [Changing tuples to list](#changing-tuples-to-list)
    - [Checking an item in a list](#checking-an-item-in-a-list)
    - [Joining tuples](#joining-tuples)
    - [Deleting tuple](#deleting-tuple)
  - [💻 Exercises: Day 6](#%f0%9f%92%bb-exercises-day-6)

# Day 6:

## Tuple

A tuple is a collection of different data types which is ordered and unchangeable(immutable). Tuples are written with round brackets,(). Once a tuple is created, we can not change its values. We can not add, insert, remove a tuple because it is not modifiable (mutable). Unlike list, tuple has few methods. Methods related to tuple:

- tuple(): to create an empty tuple
- count(): to count the number of a specified item in a tuple
- index(): to find the index of a specified item in a tuple
- - operator: to join two or more tuples and to create new tuple

### Creating Tuple

- Empty tuple: Creating an empty tuple
  ```py
  # syntax
  empty_tuple = ()
  # or using the tuple constructor
  empty_tuple = tuple()
  ```
- Tuple with initial values
  ```py
  # syntax
  tpl = ('item1', 'item2','item3')
  ```
  -
  ```py
  fruits = ('banana', 'orange', 'mango', 'lemon')
  ```

### Tuple length

We use the _len()_ method to get the length of a tuple.

```py
# syntax
tpl = ('item1', 'item2', 'item3')
len(tpl)
```

### Accessing tuple items

- Positive Indexing
  Similar to the list data type we use positive or negative indexing to access tuple items.
  ![Accessing tuple items](../images/tuples_index.png)

  ```py
  # Syntax
  tpl = ('item1', 'item2', 'item3')
  first_item = tpl[0]
  second_item = tpl[1]
  ```

  ```py
  fruits = ('banana', 'orange', 'mango', 'lemon')
  first_fruit = fruits[0]
  second_fruit = fruits[1]
  last_index =len(fruits) - 1
  last_fruit = fruits[las_index]
  ```

- Negative indexing
  Negative indexing means beginning from the end, -1 refers to the last item, -2 refers to the second last and the negative of the list length refers to the first item.
  ![Tuple Negative indexing](../images/tuple_negative_indexing.png)
  ```py
  # Syntax
  tpl = ('item1', 'item2', 'item3','item4')
  first_item = tpl[-4]
  second_item = tpl[-3]
  ```
  ```py
  fruits = ('banana', 'orange', 'mango', 'lemon')
  first_fruit = fruits[-4]
  second_fruit = fruits[-3]
  last_fruit = fruits[-1]
  ```

### Slicing tuples

We can slice out a sub tuple by specifying a range of indexes where to start and where to end in the tuple, the return value will be a new tuple with the specified items.

- Range of Positive Indexes

  ```py
  # Syntax
  tpl = ('item1', 'item2', 'item3','item4')
  all_items = tpl[0:4]         # all items
  all_items = tpl[0:]         # all items
  middle_two_items = tpl[1:3]  # does not include item at index 3
  ```

  ```py
  fruits = ('banana', 'orange', 'mango', 'lemon')
  all_fruits = fruits[0:4]    # all items
  all_fruits= fruits[0:]      # all items
  orange_mango = fruits[1:3]  # doesn't include item at index 3
  orange_to_the_rest = fruits[1:]
  ```

- Range of Negative Indexes

  ```py
  # Syntax
  tpl = ('item1', 'item2', 'item3','item4')
  all_items = tpl[-4:]         # all items
  middle_two_items = tpl[-3:-1]  # does not include item at index 3
  ```

  ```py
  fruits = ('banana', 'orange', 'mango', 'lemon')
  all_fruits = fruits[-4:]    # all items
  orange_mango = fruits[-3:-1]  # doesn't include item at index 3
  orange_to_the_rest = fruits[-3:]
  ```

### Changing tuples to list

We can change tuples to list and list to tuple. Tuple is immutable if we want to modify a tuple we should change to a list.

```py
# Syntax
tpl = ('item1', 'item2', 'item3','item4')
lst = list(tpl)
```

```py
fruits = ('banana', 'orange', 'mango', 'lemon')
fruits = list(fruits)
fruits[0] = 'apple'
print(fruits)     # ['apple', 'orange', 'mango', 'lemon']
fruits = tuple(fruits)
print(fruits)     # ('apple', 'orange', 'mango', 'lemon')
```

### Checking an item in a list

We can check an item if it exists in a list or not using _in_, it returns boolean.

```py
# Syntax
tpl = ('item1', 'item2', 'item3','item4')
'item2' in tpl # True
```

```py
fruits = ('banana', 'orange', 'mango', 'lemon')
'orange' in fruits # True
'apple' in fruits # False
fruits[0] = 'apple'
```

### Joining tuples

We can join two or more tuples using + operator

```py
# syntax
tpl1 = ('item1', 'item2', 'item3')
tpl2 = ('item4', 'item5','item6')
tpl3 = tpl1 + tpl2
```

```py
fruits = ('banana', 'orange', 'mango', 'lemon')
vegetables = ('Tomato', 'Potato', 'Cabbage','Onion', 'Carrot')
fruits_and_vegetables = fruits + vegetables
```

### Deleting tuple

It is not possible to remove a single item in a tuple but it is possible to delete the tuple itself using _del_.

```py
# syntax
tpl1 = ('item1', 'item2', 'item3')
del tpl1

```

```py
fruits = ('banana', 'orange', 'mango', 'lemon')
del fruits
```

## 💻 Exercises: Day 6

1. Create an empty tuple
2. Create a tuple containing name of your sisters and your brothers
3. Join brothers and sisters tuples and assign it to siblings
4. How many siblings do you have ?
5. Modify the siblings tuple and add the name of your father and mother and assign it to family_members
6. Unpack siblings and parents from family_members
7. Create a fruits, vegetables and animal products tuples. Join the three tuples and assign it to a variable called food_stuff.
8. Slice out the middle item or items from the food_staff list
9. Slice out the first three items and the last three items from food_staff list
10. Delete the food_staff list completely
11. Check if an item exist in a tuple:

- Check if 'Estonia' is a nordic country
- Check if 'Iceland' is a nordic country
  ```py
  nordic_countries = ('Denmark', 'Finland','Iceland', 'Norway', 'Sweden')
  ```

[<< Day 4](../05_Day/05_list.md) | [Day 7 >>]()
