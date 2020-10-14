[TOC]



# Arrays

Arrays are the simple data structures that are used for storing similar items. However, arrays in python can store mixed types of items. Arrays are often used to solve many types of problems and therefore they are very important data structure to know. 

## What is an Array? 

An array is a collection of items. The items by themselves can have different data types but they are stored in contiguous memory locations. Because they are stored together, checking through the entire collection of items is straightforward. Each position of an array has an index, which starts with `0`. Here are the strengths and weaknesses of arrays: 

*   Strengths:
    *   **Fast lookups**: Retrieving the element at a given index takes $O(1)$ time, regardless of the length of the array
    *   **Fast appends**: Adding a new element at the end of the array takes $O(1)$ time.
*   Weaknesses:
    *   **Fixed size**: Arrays have fixed size, unless we use **dynamic arrays**. Python mostly uses dynamic arrays which are also slower and take more space. 
    *   **Costly inserts and deletes**: When you insert or delete an element from an array, the elements have to be moved to fill the empty space. This takes $O(n)$ time in the worst case. 

The table below lists some important methods that are used in arrays

### `insert(index, element)`

The `insert()` method is used to insert an item at a given position. The syntax is: 

```python
arr.insert(pos, item)
```

**Example**

```python
arr = [5, 6, 6, 6, 6, 6, 5]
arr.insert(3, 10)

print(arr)
 [5, 6, 6, 10, 6, 6, 6, 5]
```

We can also insert a different data type: 

```python
arr = [4, 3, 5, 'axe']
tup = (3, 6)
arr.insert(0, tup)

print(arr)
[(3, 6), 4, 3, 5, 'axe']
```

### `.remove(element)`

The `.remove()` method is used to remove a specified element from the array. The syntax is: 

```python
arr.remove(element)
```

**Example**

```python
arr = ['Alexis', 'Josephine', 'Ella', 100]
arr.remove(100)
print(arr)

['Alexis', 'Josephine', 'Ella']
```

*   if there are two elements in an array that match, only the first occurrence will be removed and not all
*   If the element is not found, it will return an error

```python
arr.remove('Rachel')
---------------------------------------------------------------------
ValueError                      Traceback (most recent call last)
<ipython-input-486-e8ac4a6f144f> in <module>
----> 1 arr.remove('Rachel')

ValueError: list.remove(x): x not in list
```

The other way to remove an element that is index-based is the use of `.pop(index)`. 

```python
arr = ['Alexis', 'Josephine', 'Ella', 'Rachel']

# Remove the second element: 
arr.pop(1)

# Remove the last element: 
arr.pop()
```

### `.append(element)`