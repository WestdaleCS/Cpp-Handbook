<!-- DOCUMENT HEADING -->
<br />
<div align="center">
    <h3 align="center">C++ HandBook</h3>
</div>

<!-- TABLE OF CONTENTS -->
<details>
    <summary>Table of Contents</summary>
    <ol>
        <a href="#data-structures">Data Structures</a>
        <ul>
            <a href="#one-dimensional-data-structures">One-dimensional Data Structures</a>
            <ul>
                <li><a href="#vectors">Vectors</a></li>
            </ul>
        </ul>
        <a href="#loops">Loops</a>
        <ul>
            <a href="#for-loops">For Loops</a>
            <ul>
                <li><a href="#omitting-init-statement-and-end-expression">Omitting Init Statement And End Expression</a></li>
                <li><a href="#loop-through-iterables">Loop Through Iterables</a></li>
            </ul>
        </ul>
        <a href="#terminology">Terminology</a>
    </ol>
</details>

<!-- DATA STRUCTURES -->
## Data Structures

### One-dimensional Data Structure

#### Vectors
0. Header File
```cpp
#include <vector>
```
1. Initializing
```cpp
vector<int> arr;
vector<char> arr1{ 'a', 'b', 'c' };
vector<double> arr2 = { 0.1, 0.2, 0.3 };
```
2. Insertion
```cpp
arr.push_back(5) // { 5 }
arr.push_back(6) // { 5, 6 }
```


<!-- LOOPS -->
## Loops

The two common loops we will use in computing competitions are for loops and while loops.

### For Loops

#### Omitting Init Statement And End Expression

To have your counter outside of the loop:
```cpp
int i{ 0 };
	for ( ; i < arr.size();)
	{
		cout << arr[i];
		++i;
	}
```

#### Loop Through Iterables

There are multiple different ways to loop through iterables.

For a vector:
```cpp
	vector<int> arr{ 1, 2, 3, 4, 5 };
```

**__Get elements by index__**
```cpp
for (int i = 0; i < arr.size(); ++i)
	{
		cout << arr[i];
	}
```

**__Get elements with iterators (pointers)__**
```cpp
for (auto ptr = arr.begin(); ptr < arr.end(); ptr++)
	{
		cout << *ptr;
	}
```

**__Get elements using range-based for loop__**
```cpp
for (int i : arr)
	{
		cout << i;
		++i;
	}
```

<!-- Terminology -->
## Terminology

Below is an appendix if you want to check the definitions of words. All definitions were found online.

### Iterables

An object which can be looped over or iterated over with the help of a for loop. Objects like lists, tuples, sets, dictionaries, strings, etc. are called iterables. In short and simpler terms, iterable is anything that you can loop over.

### Iterators

An iterator is used to point to the memory address of the STL container classes.

### Pointers

A pointer is a variable that stores the memory address of an object. Pointers are used extensively in both C and C++ for three main purposes: to allocate new objects on the heap, to pass functions to other functions. to iterate over elements in arrays or other data structures.

### STL

It stands for Standard Template Library.
