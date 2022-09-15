# Python Data Structure Cheat Sheet

## Disclaimer: This is not mine! 
Credit goes to: https://gist.github.com/Elucidation

If you're interviewing in Python, learn how to code the following data structures / algorithms in python.

# List

lists: `a = []` or `a = list()`



# Linked List

`A -> B -> C` linked lists or `A <-> B <-> C` doubly linked lists.

Optimizes insertion/deletion as O(1). Sucks at indexing/searching O(n).

- Indexing:         Linked Lists: O(n)
- Search:           Linked Lists: O(n)
- Insertion:        Linked Lists: O(1)

#### Time Complexity:
- Indexing:         Linear array: O(1)
- Search:           Linear array: O(n)
- Optimized Search: Linear array: O(log n)

# Tuple

`a = (1,2,3)`

Nice property is it can be hashed for use in hashmaps/dictionaries.

# Array

Numpy arrays if allowed:
```
import numpy as np
a = np.array([1,2,3,4])
a = np.arange(4)
a = np.zeros(4)
...
```

#### Time Complexity:
- Indexing:         Linear array: O(1)
- Search:           Linear array: O(n)
- Optimized Search: Linear array: O(log n)

# Dictionary / Hash Map / Hash Table

`a = {}` or `a = dict()` or `a = dict(name='john', age=123)` or `a = {'name':'john', age:123'}`

You can have dictionary keys return a default value using a `defaultdict`. Very useful for counting or building multiple lists of things.

```
import collections

a = collections.defaultdict(int)
for char in 'thisisatest':
  a[char] += 1
```

#### Time Complexity:
- Indexing:         Hash Tables: O(1)
- Search:           Hash Tables: O(1)
- Insertion:        Hash Tables: O(1)

If interviewer allows, a Counter does counting for you: `collections.Counter('thisisatest').most_common(1)` -> `[('s', 3)]`

O(N) time and O(N) space worse case for N characters. Worth pointing out in an interview anyhow.

# Binary Tree

TODO

# Binary Search Tree

Unlike Binary tree, elements are ordered by some comparison (<=, >, alphabetic etc.)

#### Time Complexity:
- Indexing:  Binary Search Tree: O(log n)
- Search:    Binary Search Tree: O(log n)
- Insertion: Binary Search Tree: O(log n)

# Trie / Prefix Tree

TODO

# Dynamic Programming 

TODO

# 2D Array / List

TODO

# BFS / DFS - Breadth First Search and Depth First Search

BFS guarantees optimal path, but will search all nodes in radius # steps.
DFS can get to 'an' answer very quickly, but not necessarily optimal, for an infinite tree it may never end.

TODO

#### Time Complexity:

BFS/DFS: O(|V| + |E|)
- E is number of edges
- V is number of vertices

# Quicksort, Mergesort

You don't have to memorize how to code it fully, but be able to explain how it functions, and do simplified versions of it.

For example, given an index, how to move all values less than value at index to the left inplace.
Or given two sorted lists of ints, how to merge them.

#### Time Complexity:
- Best Case Sort: Merge Sort: O(n)
- Average Case Sort: Merge Sort: O(n log n)
- Worst Case Sort: Merge Sort: O(n log n)

- Best Case Sort: Quick Sort: O(n)
- Average Case Sort: Quick Sort: O(n log n)
- Worst Case Sort: Quick Sort: O(n^2)

# Recursive Algorithms

You're almost definitely going to get an interview question where you'll write a recursive algorithm.

Understand stack level and how it's bad (every time you recurse, that information is being stored in the stack...)

# Iterative Algorithms

You're definitely going to get an interview question where you'll write an iterative algorithm.

Know how to iterate through a string and do stuff like tell if a string is a palindrome or there is a substring with a palindrome for example.

Definitely know about two pointer iterative algorithms, like having a pointer on the start and on the end and iterating both to check if a string is a palindrome if we're allowed to change/add/remove one letter.

#### Pseudo Code of Moving Through an Array (this is why iteration is used for this)
```
Recursion                         | Iteration
----------------------------------|----------------------------------
recursive_method(array, n)        | iterative_method(array)
  if array[n] is not nil          |   for n from 0 to size of array
    print(array[n])               |     print(array[n])
    recursive_method(array, n+1)  |
```

# Others

TODO
