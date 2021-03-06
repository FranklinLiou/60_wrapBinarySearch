# 60_wrapBinarySearch

## Recall Inverse Functions and Logarithms
What is meant by:
```
count = log2n
```
This equation can also be written as:
```
2^count = n
```
- In the equation, `count` is the number that `2`, the base, must be raised to to get `n`.
- The graph looks like a curve in the first quadrant with an asymtote of `x = 0`. The graph also has an x-intercept of `1` and its rate of change decreases the greater `n` is.

## Describe the Recursive Solution
0. Find the index of a desired integer, `findMe`, within limits `high` and `low`
1. When asked to find a desired integer within two limits, the recursive abstraction will be able to find that desired integer within more narrow limits.
2. 6 parts of a general recursive solution

a. decision between base case(s) and recursive case(s)
```
if( low > hi) // base case 0

if( comparison == 0) // base case 1
```
b. instructions to solve base cases
```
return -2; // solution to base case 0

return pageToCheck; // solution to base case 1
```
c. instructions to solve recursive cases
- combination: N/A
- leftover processing: N/A
- result of recursive abstraction
```
return indexOf_recursive( findMe
                         , low
                         , pageToCheck -1); 
                         // if findMe preceeds pageToCheck

return indexOf_recursive( findMe
                         , pageToCheck -1
                         , high); 
                         // if pageToCheck preceeds findMe
```