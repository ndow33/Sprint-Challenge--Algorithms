# Analysis of Algorithms

## Exercise I

Give an analysis of the running time of each snippet of
pseudocode with respect to the input size n of each of the following:

```python
a)  a = 0
    while (a < n * n * n):
      a = a + n * n
ANSWER: O(n)
While the while loop has n^3 as the condition, we increment a by 
n^2 each time
```


```
b)  sum = 0
    for i in range(n): 
      j = 1
      while j < n: 
        j *= 2
        sum += 1
ANSWER: O(n^2)   
This is because we have a linear for loop that will run through the entire
range of n. The function j*=2 is also linear (1/2n).  
```

```
c)  def bunnyEars(bunnies):
      if bunnies == 0:
        return 0

      return 2 + bunnyEars(bunnies-1)
```

## Exercise II

Suppose that you have an n-story building and plenty of eggs. Suppose also that an egg gets broken if it is thrown off floor f or higher, and doesn't get broken if dropped off a floor less than floor f. Devise a strategy to determine the value of f such that the number of dropped + broken eggs is minimized.

Write out your proposed algorithm in plain English or pseudocode AND give the runtime complexity of your solution.

1. I'd take the 'top' floor value + the 'bottom' floor value and // by 2 
in order to find the middle floor of the building.

2. I'd then drop an egg from the middle floor. 

3. If it broke, the middle floor would become my 'top' floor
and I'd repeat 1-3/4

4. If it didn't break the middle floor would become my 'bottom' floor
and I'd repeat steps 1-3/4

The runtime complexity of the solution is O(log n)
