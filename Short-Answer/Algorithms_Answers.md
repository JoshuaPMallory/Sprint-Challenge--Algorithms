#### Please add your answers to the ***Analysis of  Algorithms*** exercises here.

## Exercise I

a) O(n)
These are basically the same equation written slightly differently. The loop will cycle as many times as it takes to equal n^3, from n^2. So whatever n is, that's the number of cycles every time.

b) O(n log n)
Takes longer than O(n), not quite n^2. Going from 10 to 100 gives back 40, then 700. Gotta be in between. 

c) O(n)
The numbers are just there to confuse. It takes as long as it takes to get through the list and nothing more.

## Exercise II
For a building of any given height, start in the middle.
If it broke, half the distance again.
If not, add half the distance.

Shorten the range based on our findings and repeat until we confirm an exact number.


```python
def drop_test(n, f):
    '''One of those few cases where recursion makes this simpler'''

    mid = int(len(n) / 2)

    if   n[mid] == f:
        return n[mid], 1
    elif n[mid]  > f:
    	new_n = n[:mid]
    else:
        new_n = n[mid:]

    ans, itr  = drop_test(new_n, f), itr + 1

```