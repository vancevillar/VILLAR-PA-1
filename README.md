# VILLAR-PA-1
### Made by : Vance Q. Villar | 2ECE-C

This repository contains Experiment 1: Introduction To Python Programming for our ECE2112 course.

# **1. Word Rotation Problem**

Create a function named `rotate_word()` that accepts a non-empty string. Move the first character of the string to the end while keeping all remaining characters in their original order. Preserve the capitalization of every character.

The following functions and methods were used in this problem:

• `text[1:]` - a string slicing operation that extracts all characters starting from index 1 to the end of the string.

Example: `"python"[1:]` --> `'ython'`

• `text[0]` - a string indexing operation that retrieves the first character of the string.

Example: `"python"[0]` --> `'p'`

• `+` - a string concatenation operator used to combine the remaining characters with the original first character placed at the end.

This string slicing and indexing were combined in order to create a single defined function that rotates the word;

```python
def rotate_word(text):
    return text[1:] + text[0]

print(rotate_word("python"))
print(rotate_word("logic"))
print(rotate_word("Code"))
print(rotate_word("A"))
```
# **2. Username Builder Problem**

Create a function named `make_username()` that accepts two strings: first name and last name. The function must convert all letters to lowercase, remove all spaces from both names, and join them using a single period (.)

The following functions and methods were used in this problem:

• `.lower()` - a built-in string method that converts all uppercase letters in a string to lowercase.

Example: `"Ada".lower()` --> `'ada'`

• `.replace(" ", "")` - a string method that replaces space characters with an empty string, removing all spaces from multi-word names.
Example: `"Ana Maria".replace(" ", "")` --> `'AnaMaria'`

• `+` - a string concatenation operator used to join the cleaned first name, a period (`"."`), and the cleaned last name into a single string.

Combining these string methods results in the final function for this problem.
```python
def make_username(first_name, last_name):
    clean_first = first_name.lower().replace(" ", "")
    clean_last = last_name.lower().replace(" ", "")
    return clean_first + "." + clean_last

print(make_username("Ada", "Lovelace"))
print(make_username("Alan", "Turing"))
print(make_username("Ana Maria", "De Leon"))
```
# **3. Bookend Swap Problem**

Create a function named `swap_bookends()` that accepts a list containing at least two elements. Unpack the list into three variables: `first` (the first element), `middle` (a list containing everything between the first and last elements), and `last` (the last element). Using these variables, return a new list in which the first and last elements have exchanged positions while keeping `middle` elements in their original order.

The following functions and methods were used in this problem:

• `first, *middle, last = items` - extended sequence unpacking that assigns the first element to `first`, the last element to `last`, and captures all intermediate elements as a list assigned to `middle`.

Example: `first, *middle, last = [1, 2, 3, 4, 5, 6]` --> `first = 1`, `middle = [2, 3, 4, 5]`, `last = 6`

• `[last] + middle + [first]` - list concatenation used to build and return a brand new list with the swapped positions without altering the original input list.

Combining extended sequence unpacking and list concatenation yields the final solution.

```python
def swap_bookends(items):
    first, *middle, last = items
    return [last] + middle + [first]

print(swap_bookends([1, 2, 3, 4, 5, 6]))
print(swap_bookends(["red", "green", "blue"]))
print(swap_bookends([8, 3]))
```

August 27, 2026 - update README output uploaded
