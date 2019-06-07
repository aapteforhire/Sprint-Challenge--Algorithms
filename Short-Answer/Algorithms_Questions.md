# Analysis of Algorithms

## Exercise I

Give an analysis of the running time of each snippet of
pseudocode with respect to the input size n of each of the following:

```
a)  a = 0
    while (a < n * n * n): 
      a = a + n * n 


```
b)  sum = 0
    for i in range(n): O(n)
      i += 1
      for j in range(i + 1, n): O(n)
        j += 1
        for k in range(j + 1, n): O(n)
          k += 1
          for l in range(k + 1, 10 + k): O(1)
            l += 1
            sum += 1
```

```
c)  def bunnyEars(bunnies):
      if bunnies == 0:
        return 0

      return 2 + bunnyEars(bunnies-1) O(n)
```

## Exercise II

Suppose that you have an _n_-story building and plenty of eggs. Suppose also that an egg gets broken if it is thrown off floor _f_ or higher, and doesn't get broken if dropped off a floor less than floor _f_. Devise a strategy to determine the value of _f_ such that the number of dropped eggs is minimized.

Write out your proposed algorithm in plain English or pseudocode and give the runtime complexity of your solution.

1) One is given an n-story building and a limitless supply of eggs
2) If an egg is dropped from floor >= f, the egg is broken.
3) If an egg is dropped from floor < f, the the egg is not broken
4) One wants to minimize the number of broken eggs


def egg_drop (floor, f):
    if floor < f:
        return 1
    else:
        return 0
