                            ARRAY IN PYTHON 
==============================================================================================================
In Python, arrays are a data structure that holds a fixed-size sequence of elements of the same type.
They are similar to lists but are more memory-efficient and provide faster access to elements. 
The main difference between arrays and lists is that arrays can only store elements of the same type,
whereas lists can contain elements of different types.

Arrays in Python are implemented using the array module,
which provides a compact way to store large amounts of numeric data efficiently.
The array module supports various data types, such as integers, floats, and characters, 
among others. Each element in the array is assigned an index starting from 0,
allowing for random access to elements.

==============================================================================================================
import array

# Create an array of integers
my_array = array.array('i', [1, 2, 3, 4, 5])

# Access elements in the array
print(my_array[0])  # Output: 1
print(my_array[2])  # Output: 3

# Modify an element
my_array[1] = 10
print(my_array)  # Output: array('i', [1, 10, 3, 4, 5])
===================================================================================================================

In the example above, we import the array module and create an array of integers using the type code 'i'. 
The second argument to the array constructor is the initial values of the array. 
We can access and modify elements using index notation, just like with lists.
check TYPE CODE for the other data types 

Arrays are useful when you need to work with large amounts of homogeneous data,
such as numerical datasets or pixel values in image processing. 
They offer improved performance and memory efficiency compared to lists,
especially when dealing with large datasets.

In Python's array module, you can specify the type of elements in an array using type codes. 
Type codes are single-character codes that represent different data types. 
Here are some commonly used type codes in the array module:
====================================================================================

                STRING IN ARRAY
==================================================================================================
Here's an example of creating an array of characters (strings) using the 'c' type code:

import array

my_array = array.array('c', ['H', 'e', 'l', 'l', 'o'])
print(my_array)

In this example, an array is created with the type code 'c'. The initializer is a list of characters representing the string 'Hello'. When you print the array, it displays the string representation of the character array.

Keep in mind that using the 'c' type code treats each character as a single byte. If you want to work with Unicode strings or store multi-byte characters, you would need to use a different approach, such as using a list or the str data type instead of the array module.
================================================================================================================

                    TYPE CODE
==================================================================
'b': Signed integer of size 1 byte (char)
'B': Unsigned integer of size 1 byte (unsigned char)
'h': Signed integer of size 2 bytes (short)
'H': Unsigned integer of size 2 bytes (unsigned short)
'i': Signed integer of size 2 or 4 bytes (int)
'I': Unsigned integer of size 2 or 4 bytes (unsigned int)
'l': Signed integer of size 4 bytes (long)
'L': Unsigned integer of size 4 bytes (unsigned long)
'f': Floating-point number of size 4 bytes (float)
'd': Floating-point number of size 8 bytes (double)
==================================================================


                    BUFFER INFO and TYPE CODE
==================================================================
Certainly! Let's discuss the concepts of buffer info and type code in the context of the array module.

Buffer Info:
In the array module, the buffer_info() method is used to retrieve information about the underlying buffer used by an array.
When called on an array object, it returns a tuple containing two values:
The memory address of the array's buffer (integer).
The number of elements in the array (integer).

example check array.py file
from array import * #import array module

value = array('i', [1, 3, 4, 5, 6, 73, 44, 34, 9]) #assign value to value var
print(value) # print the value output = array('i', [1, 3, 4, 5, 6, 73, 44, 34, 9])

print(value.buffer_info()) 

output : array('i', [1, 3, 4, 5, 6, 73, 44, 34, 9])
(139660177225888   , 9)
139660177225888 = memory adress     9 = number of elements

print(value.typecode()) 
output : will be the type used in the array in this example the type code should be i 
==============================================================================

                    ARRAY REVERSE ADN SLICING
================================================================================================
To reverse an array in Python, you can use the reverse() method if you are using the built-in list data type. However, if you are working with the array module, you can reverse the array by utilizing slicing.
Here's an example of reversing an array using both approaches:
Using the reverse() method (for lists):

from array import * #import array module

value = array('i', [1, 3, 4, 5, 6, 73, 44, 34, 9]) #assign value to value var
value.reverse()
print(value) # print the value output will be reversed = array('i', [9, 34, 44, 73, 6, 5, 4, 3, 1])

other way to reverse array is using slicing method if you remember in list concepts

ex 

from array import * #import array module

value = array('i', [1, 3, 4, 5, 6, 73, 44, 34, 9]) #assign value to value var
reversed_array = value[::-1] #this will assign to reversed_array starting from end index to starting index
print(reversed_array) # print the value output will be reversed = array('i', [9, 34, 44, 73, 6, 5, 4, 3, 1])


                                    ARRAY METHODS
======================================================================================================================
append(x): Appends the element x to the end of the array.
extend(iterable): Appends elements from the iterable to the end of the array.
insert(i, x): Inserts the element x at index i in the array.
remove(x): Removes the first occurrence of element x from the array.
pop([i]): Removes and returns the element at index i (or the last element if i is not provided).
index(x): Returns the index of the first occurrence of element x in the array.
count(x): Returns the number of occurrences of element x in the array.
reverse(): Reverses the order of elements in the array.
sort(): Sorts the elements of the array in ascending order.
=========================================================================================================================
