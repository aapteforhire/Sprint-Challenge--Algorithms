Add your answers to the Algorithms exercises here.


I. Time complexity

```
a)  a = 0                  O(1)
    while (a < n * n * n): O(n^3)
      a = a + n * n        O(n^2)

n        n^3     n^2        num_operations (net)
--       ---    ----        --------------------
1         1       1                 1
2         8       4                 2
3        27       9                 3
4        64      16                 4
5       125      25                 5

The function has a time complexity of O(n) (scales linearly with n)

```
b)  sum = 0                                        O(1)
    for i in range(n):                             O(n)
      i += 1                                       O(1)
      for j in range(i + 1, n):                    O(n-2)
        j += 1                                     O(1)
        for k in range(j + 1, n):                  O(n-4)
          k += 1                                   O(1)                      
          for l in range(k + 1, 10 + k):           O(1)
            l += 1                                 O(1)
            sum += 1                               O(1)

While each of the individual for loop steps has a time complexity ~ O(n),
the loops terminate twice as fast due to the loop variables i,j,and k incrementing 
by  1 within the loop. 

The time complexity of this code as n gets large = O(n) * O(n) * O(n) = O(n^3)


```
c)  def bunnyEars(bunnies):                         
      if bunnies == 0:                              O(1)
        return 0                                    O(1)

      return 2 + bunnyEars(bunnies-1)               O(n)

This function has a time complexity of O(n)

```

II.

'''Suppose that you have an _n_-story building and plenty of eggs. Suppose also that an egg gets broken if it is thrown off floor _f_ or higher, and doesn't get broken if dropped off a floor less than floor _f_. Devise a strategy to determine the value of _f_ such that the number of dropped eggs is minimized.

Write out your proposed algorithm in plain English or pseudocode and give the runtime complexity of your solution.'''

Given:
1) One is given an n-story building and a limitless supply of eggs
2) If an egg is dropped from floor >= f, the egg is broken.
3) If an egg is dropped from floor < f, the the egg is not broken
4) One wants to minimize the number of dropped eggs.


Pseudocode Algorithms:

def egg_break():
'''Function that determines if an egg is broken, returns a Boolean''' 

def egg_break_count (f, num_drops):
'''Determines the number of egg breaks for a given floor'''
    count = 0
    for i in range(num_drops):
        if egg_break:
            count +=1
    return count

def minimize_drops():
'''Finds the floor that minimizes the number of drops'''
    min_floor = 0
    count = 0
    num_drops = # Insert number of trials
    min_count = # Insert Large number
    for i in range(_n_):
        count = egg_break_count(i, num_drops)
        if count < min_count:
            min_count = count
            min_floor = i
    return min_floor


egg_break           O(1)
egg_break_count     O(num_drops)
minimize_drops      O(_n_)

Time complexity ~ O(n^2)

