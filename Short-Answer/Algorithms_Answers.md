#### Please add your answers to the ***Analysis of  Algorithms*** exercises here.

## Exercise I

a) ANSWER: O(n)
While the while loop has n^3 as the condition, we increment a by 
n^2 each time


b) ANSWER: O(n^2)   
This is because we have a linear for loop that will run through the entire
range of n. The function j*=2 is also linear (1/2n).  


c) ANSWER: O(N)

## Exercise II

1. First, check to see if the 'top' floor value is > the 'bottom' floor value.
2. If it is...

  1a. I'd take the 'top' floor value + the 'bottom' floor value and // by 2 
  in order to find the 'middle' floor of the building.

  2a. I'd then drop an egg from the middle floor. 

  3a. If it is broken, the middle floor would become my 'top' floor
  and I'd return to step one and start the process again

  4a. If it didn't break the middle floor would become my 'bottom' floor
  and I'd return to step one and start the process again

3. If it's not...
  1b. We can return the value of the top or bottom floor as they should be the same.

We have found the value of floor f

The runtime complexity of the solution is O(log n) as this is a binary search
