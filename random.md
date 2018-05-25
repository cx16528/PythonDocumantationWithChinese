# Numpy.random中shuffle与permutation的区别

## shuffle与permutation的区别

- 函数shuffle与permutation都是对原来的数组进行重新洗牌（即随机打乱原来的元素顺序）；区别在于shuffle直接在原来的数组上进行操作，改变原来数组的顺序，无返回值。而permutation不直接在原来的数组上进行操作，而是返回一个新的打乱顺序的数组，并不改变原来的数组。

### 示例：
```python
a = np.arange(12)  
print a  
np.random.shuffle(a)  
print a  
print   
a = np.arange(12)  
print a  
b = np.random.permutation(a)  
print b  
print a  
```

### 输出：
```python
[ 0  1  2  3  4  5  6  7  8  9 10 11]  
[11  6  4 10  3  0  7  1  9  2  5  8]  
      
[ 0  1  2  3  4  5  6  7  8  9 10 11]  
[10  4  8 11  1  7  6  2  0  9  5  3]  
[ 0  1  2  3  4  5  6  7  8  9 10 11] 
```
