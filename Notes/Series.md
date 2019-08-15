# Series

### 1 import numpy和pandas
```
import numpy as np
import pandas an pd
```

### 2 创建Series的几种方法

方法1：直接使用数组作为参数
```
s1 = pd.Series([1,2,3,4])
print(s1)
>>> 
0 1
1 2
2 3
3 4
dtype: int64
```
方法2：使用numpy作为参数
```
s2 = pd.Series(np.arange(10))
```
方法3：使用字典作为参数
```
s3 = pd.Series({'1': 1, '2': 2, '3': 3})
```
方法4：指定索引建立Series
```
s4 = pd.Series([1,2,3,4], index=['A','B','C','D'])
print(s4)
>>> 
A 1
B 2
C 3
D 4
dtype: int64
```
----


### 3 Series.values
```
s1.values
>>> array([1, 2, 3, 4])
```
----


### 4 Series.index
```
s1.index
>>> RangeIndex(start=0, stop=4, step=1)
```
---

### 5 Series和Python中Dict的相互转化
在2.方法3中我们使用Dict作为参数，可以生成Series，同样的也可以将Series转换成Dict
```
s4.to_dict()
print(s4)
>>> {'A': 1, 'B': 2, 'C': 3, 'D': 4}
```
