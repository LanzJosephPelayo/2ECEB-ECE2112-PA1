# ECE-2112-PA-1

**Made by: Lanz Joseph S. Pelayo || 2ECE-B**

# Introduction
This repository contains an explanation of the code for the programming assignment, which the author has made available for the viewer to see. Specifically, the contents of this repository aim to answer the Programming Assignment with its 3 problems in the Academic year of 2026-2027 in ECE 2112. This aims for viewers to tell how the author masters the basic functions of Python, specifically Module 1.


# A) Word Rotation Problem

Instructions:
Create a function named rotate word() that accepts a non-empty string. Move the first character
of the string to the end while keeping all remaining characters in their original order. Preserve the
capitalization of every character.

The following methods were used in this problem to create a unique function:

• Slicing - It enables the extraction of specific values or items within a text, set, subset, or list in sequence without tampering with the original data.

Example: `text[1:] + text[0]`
        

In this part, the author used slicing in order for the first letter to switch places at the end, allowing the rest of the letters in the string to go first. It basically extracted the 2nd element from the string til the very last, hence it's blank, so that they don't need to manually input how long the string is. It was then added to the text without the first letter, and the first letter was added at the end with an index of 0.

This method itself allows us to create the word rotation function by adding the two strings through the use of slicing from the original word where it was combined, which leaves us with the first letter going to the last place of the word.

``` python
def rotate_word(text):
    out = text[1:] + text[0] # ->iterates the 2nd element of the string til the end and combines it with the first element in the end where its combines into the variable out.
    return out

print(rotate_word("python")) ---> ythonp
```

# B) USERNAME BUILDER PROBLEM
Create a function named make username() that accepts two strings: first name and last name. The
function must:
1. convert all letters to lowercase;
2. remove all spaces from the first name;
3. remove all spaces from the last name; and
4. join the processed first and last names using one period (.).

   
The following methods were used in this problem to create a unique function:

• `.lower()` - Makes the string value lowercase.
This allows the function to make every name in lower case form as per instructions and to make it neat and readable instead of various upper and lower case within the string.

Example: 
``` python
first = MBAPPE
first = first.lower()-->mbappe
```
• `.replace(" ","")` - Allows o replace specific text to another text
This allows the function to remove spaces by automatically replacing them with an empty text, so it can compress the string together.
Example:
``` python
first = jane doe
first = first.replace(" ","")--> janedoe
```

By combining these methods, which lowercases the strings of the first and last name, and removes the spaces by replacing them, it is then added together into one unified string to be output. This allows to make our Username Builder Function.
``` python
def make_username(first, last):
    first = first.lower() #--> makes every text in the string inputted lowercase
    last = last.lower() #--> makes every text in the string inputted lowercase
    first = first.replace(" ", "")  #--> makes the spaces to removed by replacing it with nothing
    last = last.replace(" ", "") #--> makes the spaces to removed by replacing it with nothing
    out = first + "." + last #--> Combines the first and last name into a structured username 
    return out #--> Returns the username

print(make_username("Ada", "Lovelace")) --> ada.lovelace
```

# C. BOOKEND SWAP PROBLEM
Create a function named swap bookends() that accepts a list containing at least two elements. Unpack
the list into three variables:
• first – the first element;
• middle – a list containing everything between the first and last elements; and
• last – the last element

The following methods were used in this problem to create a unique function:

• `Extended Iterable` - Allows to capture or extract a string from the first, middle, and end of a set and store it in a variable.

In the function that the author made, the command `first` extracts the first element from index 0 of the list, the `*middle` allows everything in the list within the middle to be extracted, where the first and last elements of the list, and `last` extracts the last element from index -1.

By just using these commands, where the `last` element will become first, add it to the `*middle` elements, and the `first` element will be the last, this allows  us to make a function where the first and last elements switch and return a new list without affecting the old and original list from being tampered with.

```python
def swap_bookends(items):
    first, *middle, last = items # first, middle and last elements were captured from the set into their respective variables
    return [last] + middle + [first] # returning the  swap book ends function by swapping the first and last elements to formulate a new list for the function required without affecting the original list or set

print(swap_bookends(["red", "green", "blue"])) --> ['blue', 'green', 'red']
```

Thank you for reading!

To see the main python program for Programming Assignment 1, click this link
https://github.com/LanzJosephPelayo/2ECEB-ECE2112/blob/main/Programming%20Assignment%20%231.ipynb
and download the raw file. Open on Jupyter Notebook, then run all cells.

README file Version History:

August 27, 2027 - 1st README output uploaded.




