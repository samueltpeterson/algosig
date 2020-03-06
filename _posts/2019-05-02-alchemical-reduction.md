---
title: Alchemical Reduction (Advent of Code 2018)
category: "AlgoSIG 3"
link: https://adventofcode.com/2018/day/5
author:
tags:
  - unsolved
---

## Description

You'll need to get your own input for this challenge from [this Advent of Code problem]({{ page.link }}).

## Solution

```python
is_pair = lambda x,y: x != y and x.lower() == y.lower()

def alchemical_reaction(string):
    return scan(list(string),0)
    
def scan(polys,i):
    if is_pair(polys[i],polys[i+1]):
        del polys[i:i+2]
        scan(polys,max(0,i-1))
    if (i < (len(polys ) - 2)):
        scan(polys,i+1)
    return len(polys)
```
