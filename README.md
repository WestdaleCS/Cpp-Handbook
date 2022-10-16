<!-- DOCUMENT HEADING -->
<br />
<div align="center">
    <h3 align="center">C++ HandBook</h3>
</div>

<!-- TABLE OF CONTENTS -->
<details>
    <summary>Table of Contents</summary>
    <ol>
        <a href="#data-types">Data Types</a>
        <ul>
            <a href="#one-dimensional-data-structures">Strings</a>
        </ul>
        <a href="#data-structures">Data Structures</a>
        <ul>
            <a href="#one-dimensional-data-structures">One-dimensional Data Structures</a>
            <ul>
                <li><a href="#vectors">Vectors</a></li>
                <li><a href="#linked-lists">Linked Lists</a></li>
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



<!-- DATA TYPES -->
## Data Types

### Strings
Initializing and passing strings are expensive. If have to and for read only, use `string_view` instead.

```cpp
#include <string>
```
1. Initializing
```cpp
string sentence { "Hello, world!" };
sentence = "Hello, xxx!";
```
2. Length
```cpp
cout << sentence.length(); // 13
```



<!-- DATA STRUCTURES -->
## Data Structures

### One-dimensional Data Structure

#### Vectors
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

#### Linked Lists
Imagine linked lists as a train: if you know where one car is, you will know where the next car is (unless it is the end of the train).
Two common container adaptors of linked lists we need to use in this club will be stack, and queue.

##### Stacks
It is a last in first out (LIFO) structure which you put one element in from the top and it would be removed from the top only. The encapsulated object by default is deque, but can also be vector and list.
```cpp
#include <stack>
```
1. Initializing
```cpp
stack<int> numbers;
```
2. Insertion
```cpp
numbers.push(2); // 2
numbers.push(9); // 9 -> 2
numbers.push(8); // 8 -> 9 -> 2
```
3. Deletion
```cpp
numbers.pop(); // 9 -> 2
```
4. Get Element
```cpp
int ele;
ele = numbers.top(); // ele == 9
```
5. Size
```cpp
int size{ numbers.size() }; // 2
```
6. If Empty
```cpp
cout << numbers.empty(); // false
```

##### Queues
It is a first in first out (FIFO) structure where element is inserted from the back and is deleted from the front (top).
```cpp
#include <queue>
```
1. Initializing
```cpp
queue<int> numbers;
```
2. Insertion
```cpp
numbers.push(2); // 2
numbers.push(9); // 2 -> 9
numbers.push(8); // 2 -> 9 -> 8
```
3. Deletion
```cpp
numbers.pop(); // 9 -> 8
```
4. Get Element
```cpp
cout << numbers.front(); // 9
cout << numbers.back(); // 8
```
5. Size
```cpp
int size{ numbers.size() }; // 2
```
6. If Empty
```cpp
cout << numbers.empty(); // false
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

**Get elements by index**
```cpp
for (int i = 0; i < arr.size(); ++i)
	{
		cout << arr[i];
	}
```

**Get elements with iterators (pointers)**
```cpp
for (auto ptr = arr.begin(); ptr < arr.end(); ptr++)
	{
		cout << *ptr;
	}
```

**Get elements using range-based for loop**
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
