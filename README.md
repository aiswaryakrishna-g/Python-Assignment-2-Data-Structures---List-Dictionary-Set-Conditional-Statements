[README_Assignment2.md](https://github.com/user-attachments/files/34970741/README_Assignment2.md)
# Python Assignment 2: Data Structures – List, Dictionary, Set & Conditional Statements

**Author:** Aiswarya Krishna G
**Tools:** Python 3, Jupyter Notebook

## Overview

This assignment covers three core Python data structures (**lists, dictionaries and sets**) and **conditional statements** (`if`, `elif`, `else`). It includes creating, modifying and accessing each structure, and a performance category program based on user input.

## Concepts Covered

- List creation, modification (`append`, `insert`, `remove`, `pop`, `extend`, `sort`) and access (indexing and slicing)
- Built-in functions: `max()`, `min()`, `sum()`
- Dictionary creation, access, addition, update, and `keys()`, `values()`, `items()`
- Sets: uniqueness of elements, lack of indexing, `union` and `intersection`
- Conditional statements with `if`, `elif`, `else` and input validation

---

## Part 1: Lists

### 1. List Creation

```python
age_list = [24, 25, 26, 27, 28]
name_list = ["Priya", "Arjun", "Meena", "Karthik", "Divya"]
```

### 2. List Operations

```python
name_list.append("Yazhini")      # a. append
age_list.insert(2, 30)           # b. insert 30 at index 2
name_list.remove("Yazhini")      # c. remove
age_list.pop()                   # d. pop last element
age_list.extend([29, 30, 26])    # e. extend
age_list.sort(reverse=True)      # f. sort descending

print("Max age:", max(age_list))     # g.
print("Min age:", min(age_list))
print("Sum of ages:", sum(age_list))
```

**Output**
```
Max age: 30
Min age: 24
Sum of ages: 217
```

Final `age_list`: `[30, 30, 29, 27, 26, 26, 25, 24]`

### 3. Accessing List Elements

```python
print(name_list[0])       # a. first element
print(name_list[-1])      # b. last element
print(name_list[2:5])     # c. index 2 to 4
print(name_list[::-1])    # d. reverse order
```

**Output**
```
Priya
Divya
['Meena', 'Karthik', 'Divya']
['Divya', 'Karthik', 'Meena', 'Arjun', 'Priya']
```

---

## Part 2: Dictionary

```python
student_marks = {"Priya": 88, "Arjun": 75, "Meena": 92, "Karthik": 67, "Divya": 81}  # a.

print(student_marks["Meena"])      # b. access a mark
student_marks["Janani"] = 80       # c. add new student
student_marks["Arjun"] = 82        # d. update a mark

print(student_marks.keys())        # e.
print(student_marks.values())
print(student_marks.items())
```

**Output**
```
92
dict_keys(['Priya', 'Arjun', 'Meena', 'Karthik', 'Divya', 'Janani'])
dict_values([88, 82, 92, 67, 81, 80])
dict_items([('Priya', 88), ('Arjun', 82), ('Meena', 92), ('Karthik', 67), ('Divya', 81), ('Janani', 80)])
```

---

## Part 3: Sets

### a. Creating `my_set`

```python
my_set = set(['a', 'e', 'i', 'o', 'u', 'a', 'a', 'i'])
print(my_set)
```

**Output** (order may vary): `{'a', 'e', 'i', 'o', 'u'}`

**Explanation:** A set stores only unique elements, so the repeated `'a'` and `'i'` are removed. Sets are also unordered, so the print order can differ between runs.

### b. Changing a value by index

```python
try:
    my_set[4] = 's'
except TypeError as e:
    print("Error:", e)
```

**Output:** `Error: 'set' object does not support item assignment`

**Explanation:** Sets are unordered and have no index positions, so individual elements cannot be accessed or changed with `my_set[4]`.

### c & d. Union and Intersection

```python
set1 = {1, 3, 5, 7, 9}
set2 = {2, 3, 5, 8, 10}

print("Union:", set1.union(set2))
print("Intersection:", set1.intersection(set2))
```

**Output**
```
Union: {1, 2, 3, 5, 7, 8, 9, 10}
Intersection: {3, 5}
```

---

## Part 4: Conditional Statements – Performance Category Program

```python
score = float(input("Enter your score (0 to 10): "))

if score < 0 or score > 10:
    print("Invalid score! Please enter a value between 0 and 10.")
elif score > 7:
    print("Above Average: Excellent work! Keep up the great performance.")
elif score >= 4:
    print("Average: Good effort! Keep practicing, there's room for improvement.")
else:
    print("Below Average: Need to improve your performance, consistent practice will lead to better results.")
```

**Category rules**

| Score | Category |
|---|---|
| Greater than 7 | Above Average |
| 4 to 7 (inclusive) | Average |
| Less than 4 | Below Average |

**Sample Output**
```
Enter your score (0 to 10): 7
Average: Good effort! Keep practicing, there's room for improvement.
```

---

## Key Takeaways

- Lists are **mutable** and ordered; methods like `append()`, `insert()` and `sort()` change the list in place.
- Slicing uses `[start:stop]`, where `stop` is excluded, so `name_list[2:5]` returns indices 2 to 4.
- Dictionaries store key-value pairs; assigning to an existing key updates it, and a new key adds an entry.
- Sets contain **unique, unordered** elements and cannot be indexed.
- In an `if/elif/else` chain, the order of conditions matters because the first true condition runs.

## How to Run

1. Open the notebook in Jupyter Notebook.
2. Run the cells in order (**Shift + Enter**), or use **Kernel → Restart & Run All**.
3. Enter a score when prompted in the last cell.
