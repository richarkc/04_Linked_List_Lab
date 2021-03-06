04_Linked_List_Lab
==================

Implement a simple linked list using pointers and classes.

Requirements
------------

1. Add, remove, get, and set should be O(1) if `i == 0` or if `i == size()-1`
2. Add, remove, get, and set should throw a string exception if `i >= size()`. Find should throw a string exception if `i > size()`
3. Do not leak memory (make sure remove and the destructor do the right thing)
4. `size()` is O(1) time (keep track of the numItems when you add or remove, so you can just return the variable)

Reading
=======
"Open Data Structures," Chapter 3, up through section 2 (DLList), http://opendatastructures.org/ods-cpp/3_Linked_Lists.html

Questions
=========

#### 1. Which of the above requirements work, and which do not? For each requirement, write a brief response.

1. Works, only iterates once for the first and last elements, forwards and backwards respectively.
2. Properly throws string exceptions.
3. No memory is leaked, destructor deletes all nodes.
4. Works, size() simply returns numItems.

#### 2. If we did an ArrayList instead of a LinkedList, which of the public methods would be faster, and which would be slower? Explain your answer.

Get() would be faster as we don't have to iterate through the array, Add() would be slightly faster unless the array is resized, then it is slower.
Remove() would be slower as the array has to compensate for the missing element by moving the elements in front of it, and set() would be faster 
for the same reason as Get().

#### 3. What is one question that confused you about this excercise, or one piece of advice you would share with students next semester?

-> operator was a little confusing at first, so I would say make sure that you understand it before you attempt to implement this.