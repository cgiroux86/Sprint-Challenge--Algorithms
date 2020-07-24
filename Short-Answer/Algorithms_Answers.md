#### Please add your answers to the **_Analysis of Algorithms_** exercises here.

## Exercise I

a) This will be an O(n) runtime. This is because the loop is going to run linear to the input size n, since the n^3 and n^2 cancel out to be n.

b) This is O(n log(n)) because the inner loop is going to run half the times for every iteration of the outer loop.

c) This is O(n) because there is only one recursive call, which is reducing the input time by 1 each time, therefore a linear relationship

## Exercise II

This is a binary search problem, which means it will have an O(log n) runtime complexity. The reason we can use binary search effectively here, is because a building can be thought of as an inorder structure. We can think of it like this:
if we have a 20 story building, we go up to level 10 and drop an egg.
We then have two choices: either the egg is broken or it's not.

- if it's broken, we move down to level 5 and try again
  -if it's not broken, we move up to level 15 and try and again
  We can continue this process, splitting the difference, until we find the optimal floor to drop the egg off.

Function Egg Drop(n):
prev = n
floor = n/2
While True:
if floor - prev == 1:
drop egg
if result is ok:
return floor
else:
return prev
else:
drop egg from floor
if result is ok:
prev = floor
floor = floor + floor/2
else:
floor /= 2
