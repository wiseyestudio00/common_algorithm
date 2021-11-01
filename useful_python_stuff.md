## collections.Counter
Takes in an iterable or mapping.

```
counters = [1, 1, 2, 2, 3, 3, 4]

c = collections.Counter(counters)
```

Basically returns a dictionary. However, it doesn't raise `key-error` when indexing a non-existing key. Just return 0.

```
counters = [1, 1, 2, 2, 3, 3, 4]

c = collections.Counter(counters)

c[1] # return 2
c[2] # return 2
c[4] # return 1
c[0] # return 0
```

# building two dimensional array
ex: a 2 x 3 arrays

```
[?, ?]
[?, ?]
[?, ?]
```

```
col_count = 2
row_count = 3

arrays = [[0 for x in range(col_count)] for y in range(row_count)]
```