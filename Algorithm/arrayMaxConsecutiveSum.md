
# `arrayMaxConsecutiveSum(inputArray, k))`

## Problem
- size `l`의 배열이 있을 때, 해당 배열로부터는 크기 `k`의 연속된 배열을 `l-k+1`개 만들 수 있다. 
- 만들 수 있는 배열 중에서 가장 큰 합은 무엇인가? 

## solution
### slower, but pythonic way

```python
def arrayMaxConsecutiveSum1(inputArray, k):
    kxs = [inputArray[i:i+k] for i in range(0, len(inputArray)-k+1)]
    return max(map(lambda xs: sum(xs), kxs))
```
