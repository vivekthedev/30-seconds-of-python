---
title: generate_password
tags: utility,intermediate
---

Generate a strong string password with a few lines.

- Get all printable characters from `string.printable`.
- Remove all whitespace characters using `string.whitespace` and set operations .
- Use `list()` to convert the `set()` to a regular list.
- Return a sample of the `list()` using `random.sample` in  a string form.

```py
from string import printable as pr, whitespace as wh
from random import sample

a = list(set(pr) - set(wh))

def generate_password(l = 12):
    return ''.join(sample(a,l))

```

```py
generate_password() #v}+?X`f|9b:%
generate_password(20) #oQCnYg1)Ev`wc2B+XLMA
```
