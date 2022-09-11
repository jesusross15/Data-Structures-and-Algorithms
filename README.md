# Data-Structures-and-Algorithms
Stacks and Queues are nothing new they are simply arrays with restrictions.

Fundamental Data Types. We don’t implement them directly but they are the fundamental building blocks of many algorithms. 

Value? Collection of objects.                       Intent is clear when we insert

Operations:

1. insertion
2. deletion
3. iteration
4. test if empty
5. 

Stacks and Queues are tools uses for handling TEMPORARY data (serve as temporary containers)

- imformation that doesn’t have any meaning after it is processed so you can throw it away once you’re done w it like the food order at a diner
    - each has a special focus on the order in which the data is handled though
    

![Screen Shot 2022-09-11 at 12.39.51 PM.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/65e7d89f-3794-4427-b0c9-85ab8f7d2072/Screen_Shot_2022-09-11_at_12.39.51_PM.png)

STACK = LAST IN FIRST OUT (LIFO)

QUEUE = FIRST IN FIRST OUT (FIFO)

The idea behind this is to completely seperate the interface and implementation 

- when you have a precicely defined DS like these you want to completely seperate the details of the implementation from the client
    - client code should ONLY perfrom the basic operations
    

# Stack

## Overview

- an abstract data type (ADT)
    - a type for objects where only behavior is defined but not implementation
        - can be implemented using whatever you want: array, structure, pointer and linked list etc.
            - can either be fixed size or dynamically sized (array is fixed)
            

A stack stores data the same way an array does, the only thing is that stacks have the following constraints:

- data can be INSERTED ONLY at the END of a stack
- data can be DELETED ONLY from the END of the stack
- only the last element of a stack can be read

Think of stack as an actual stack of dishes; you can’t look at the face of any dish other than the top one. Likewise you can’t add a dish except to the top of the stack nor can you remove any dish besides the one at the top.

- end of stack = top
- beginning of a stack = bottom

Inserting a new element onto a stack is called “pushing onto the stack”

Removing a element from the stack is called “popping from the stack”

### Picture of a stack

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/6080a982-5e34-45d3-9f24-c43b565f9449/Untitled.png)

## LIFO- LAST IN FIRST OUT

all this means is that the LAST item PUSHED onto a stack is always the first item POPPED from it

## Why does this DS exist?

Stacks are a DS that is used to hold TEMPORARY data

Real world uses:

back/forward button on browsers

undo/redo button in a text editor (word, docs, excel, vs code)

Stack Implementation using a list

```python
# Python program to demonstrate stack implementation using list
 
stack = []
 
# append() function to push element in the stack
stack.append('a')
stack.append('b')
stack.append('c')
 
print('Initial stack')
print(stack)
 
# pop() function to pop element from stack in LIFO order
print('\nElements popped from stack:')
print(stack.pop())
print(stack.pop())
print(stack.pop())
 
print('\nStack after elements are popped:')
print(stack)
 
# uncommenting print(stack.pop()) will cause an IndexError as the stack is now  empty
```

```python
class myStack:
     def __init__(self):
         self.container = []  
         
     def isEmpty(self):
         return self.container.size() == 0  

     def push(self, item):
         self.container.append(item)  
         
     def pop(self):
         return self.container.pop() 
         
     def size(self):
         return len(self.container)
```

The functions associated w/ the stack are>

- **empty()** – Returns whether the stack is empty – Time Complexity: O(1)
- **size()** – Returns the size of the stack – Time Complexity: O(1)
- **top() / peek()** – Returns a reference to the topmost element of the stack – Time Complexity: O(1)
- **push(a)** – Inserts the element ‘a’ at the top of the stack – Time Complexity: O(1)
- **pop()** – Deletes the topmost element of the stack – Time Complexity: O(1)
