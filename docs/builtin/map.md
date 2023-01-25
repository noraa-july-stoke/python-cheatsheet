---
title: Python map() built-in function - Python Cheatsheet
description: Return an iterator that applies function to every item of iterable, yielding the results. If additional iterable arguments are passed, function must take that many arguments and is applied to the items from all iterables in parallel. With multiple iterables, the iterator stops when the shortest iterable is exhausted. For cases where the function inputs are already arranged into argument tuples.
---

<base-title :title="frontmatter.title" :description="frontmatter.description">

# Python map() built-in function

</base-title>

<base-disclaimer>
  <base-disclaimer-title>
    From the <a target="_blank" href="https://docs.python.org/3/library/functions.html#map">Python 3 documentation</a>
  </base-disclaimer-title>
  <base-disclaimer-content>
   Return an iterator that applies function to every item of iterable, yielding the results. If additional iterable arguments are passed, function must take that many arguments and is applied to the items from all iterables in parallel. With multiple iterables, the iterator stops when the shortest iterable is exhausted. For cases where the function inputs are already arranged into argument tuples.
  </base-disclaimer-content>
</base-disclaimer>

  

###Basics

The map function, map(function, iterable) takes in one or more iterables, a 'callback function' (often a lambda), and returns a "Map Object". The map object contains the result of the map function applying the callback to each element in the iterable arguments. Map iterates over the provided iterable objects simultaneously. As in, at every step, "i" in the map function, the element at index "i" of each iterable will be available to the map function at that time. You will often want to cast the resultant map object to a list, tuple, or another form of object that is more convenient to work with once you are finished mapping.
  
  
Input Parameters:

Function: takes the item (or items) at the index corresponding to the current step of the Map and gives the return result as an item to store in the Map Object. The type of element stored to the map object will be identical to the type returned from the function.
  
Iterable(s): tuple, list, range, dictionary, set, string.
  
###A very simple example:
  
 ```python
  
 ```
def double_map(func, iter):
  my_map = map(func, iter)
  return list(my_map)
  
def double(element):
  return element*2
  
nums = [1,2,3,4]
  
print(double_map(double,nums))

 ```



