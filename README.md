# Big O Notation and Complexity
Big O notation and computational complexity lesson/review for WWC DC algorithms meetup.

## The Basics
### What is big O?
Big O is a convention and notation used to describe the complexity of an algorithm relative to the size of its input. It is most commonly used to describe the run time of an algorthim, but can also be used to describe the space or memory constraints of an algorithm. It can also be called *asymptotic notation* or *Bachmann-Landau notation*. The O refers to the _order_ of a function.

### What does it look like?
Usually, the variable _n_ is used to represent the input to an algorithm. Here are some big O notations that you will see often.

*O(1)* - constant

This means that the algorithm takes the same amount of time to run no matter the size of the input. 

Example: accessing the nth item in an array.

```
a[0]
a[10000]
a[100000]
```

*O(n)* - linear

This means that the algorithm's run time varies directly in proportion to the size of its input. 

Example: searching through an unsorted array.

```
def search(arr, target):
  # returns True if target is in arr, False otherwise
  for item in arr:
    if item == target:
      return True
  return False
```

*O(n^2)* - quadratic

This means that the algorithm's run time varies in proportion to the square of its input. 

Example: insertion sort

```
def insertion_sort(arr):
 # sorts arr in ascending order
 for i in range(len(arr)):
  j = i
  while j > 0 and arr[j - 1] > arr[j]:
    # swap arr[j] and arr[j - 1]
    temp = arr[j]
    arr[j] = arr[j - 1]
    arr[j - 1 ] = temp
    j = j - 1
  return arr
```

*O(n^c)* - polynomial


*O(log n)* - logarithmic
Complexity varies in proportion to the log of the input. The base of the log is generally 2; that is, the problem set is reduced by half at every iteration of the algorithm.

Example: Binary search on a sorted array
```
def binary_search(arr, target):
  # returns True if target is in arr, False otherwise
  if len(arr) == 0:
    return False
  else:
    midpoint = len(arr) / 2
    if arr[midpoint] < target:
      binary_search(arr[(midpoint + 1):], target)
    elif arr[midpoint] > target
      binary_search(arr[0:midpoint], target)
    else:
      # arr[midpoint] == target
      return True
```

*O(n log n)* - loglinear

*O(c^n)* - exponential

This means that

### What does complexity mean?
It is often said that big-O notation is used to describe the complexity of an algorithm. But it's important to note that in this case, complexity has a very specific definition of _how many calculations a program has to make relative to its input_, if we're talking about run time, and _how much space it requires relative to its input_ if we're talking about space. A more efficient, and thus less _complex_, according to this definition, algorithm, may actually look more complicated than a less efficient one.

### How accurate do I have to be?

## Let's Give it a Try
Give the big O notations for the following.

## Worst, Best, and Average Case

## Big O Notation for Common Algorithms

## In Conclusion
### When and how might this come up?

### Further reading
https://en.wikipedia.org/wiki/Big_O_notation

http://bigocheatsheet.com/

https://www.interviewcake.com/article/java/big-o-notation-time-and-space-complexity

https://www.khanacademy.org/computing/computer-science/algorithms/asymptotic-notation

https://rob-bell.net/2009/06/a-beginners-guide-to-big-o-notation/
