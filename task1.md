# Datawhale Python基础训练营作业（1）

## 变量、运算符与数据类型

**注释**


```python
# 我是一个python的注释！我是绿色的！
```


```python
"""
我是多行注释，我是红色的！
"""
```




    '\n我是多行注释，我是红色的！\n'



## 运算符

### 算术运算符


```python
print(1+1) #加法
```

    2
    


```python
print(1*1)#乘法
```

    1
    


```python
print(1-1)#减法
```

    0
    


```python
print(3/2)#除法
```

    1.5
    


```python
print(3//2)#整除（地板除）
```

    1
    


```python
print(3%4)#取余
```

    3
    


```python
print(3**3) #幂
```

    27
    

### 比较运算符


```python
print(2>1)
```

    True
    


```python
print(2>= 4)
```

    False
    


```python
print(3 == 4) #3等于4嘛？
```

    False
    


```python
print(1<2) #1小于等于2嘛？
```

    True
    


```python
print(5 <= 2) #5小于等于2嘛？
```

    False
    


```python
print(3!=5) #3不等于5嘛？
```

    True
    

### 逻辑运算符


```python
print(3>2) and (3<5) # 3大于2且3小于5
```

    True
    


```python
print(1>3)or (9<2)
```

    False
    




    False




```python
print(not (2>1))
```

    False
    

### 位运算符

这部分还需进一步学习二进制算法。


```python
print(bin(4))
```

    0b100
    


```python
print(bin(5))
```

    0b101
    


```python
print(bin(~4))
```

    -0b101
    


```python
print(bin(4&5))
```

    0b100
    


```python
print(bin(4|5))
```

    0b101
    


```python
print(bin(4<<2))
```

    0b10000
    


```python
print(bin(4^5))
```

    0b1
    


```python
print(bin(4>>2))
```

    0b1
    

### 三元运算法


```python
#这是一个特别冗余的表达方式！
x,  y = 4, 5
if x < y:
    small = x
else:
    small = y

print(small)
```

    4
    


```python
#用三元操作符可以做简化如下：

x, y = 4, 5

small = x if x < y else y
print(small)
```

    4
    


```python
letters = ['A','B','C']

if 'A' in letters:
    print('A'+' exists')

if 'H' not in letters:
    print('H' + ' not exists')
```

    A exists
    H not exists
    

比较两个变量均指向不可变的类型


```python
a = 'hello'
b = 'hello'
print(a is b, a == b)
print(a is not b, a != b)
```

    True True
    False False
    

比较两个变量均指向可变类型, 这里需要注意以下a is b 和 a == b 运算的区别，is对比的是内存的地址， ==对比的是变量之间的值！


```python
a = ['hello']
b = ['hello']
print(a is b, a == b)
print(a is not b, a != b)
```

    False True
    True False
    

### 运算符的优先级

- 规则1：一元运算符比其他运算符优先！
- 规则2：运算顺序为：算术运算>移位运算>位运算
- 逻辑运算是最后的！


```python
print(-4 ** 2)
```

    -16
    


```python
print(3 ** -3)
```

    0.037037037037037035
    


```python
print(1<< 3 + 3 & 7)
```

    0
    


```python
print(-3 * 2 + 5 / -2 - 4)
```

    -12.5
    


```python
print(3 < 4 and 4 < 5) 
```

    True
    

## 变量和赋值

- 变量相当于一张白纸，要给他赋值！
- 变量名可以是数字、字母、下划线，不能以数字开头！
- 大小写敏感


```python
teacher = 'a'

teacher
```




    'a'




```python
first = 1
second = 2

third = first + second

third
```




    3




```python
myTeacher = "老马的程序人生"
yourTeacher = "小马的程序人生"
ourTeacher = myTeacher + ',' + yourTeacher
print(ourTeacher)
```

    老马的程序人生,小马的程序人生
    

## 数据类型和变换

数据类型一共有三种，分别:
- int整型
- float浮点型
- bool布尔型。


```python
a = 1110

type(a)
```




    int



Python都是对象，有属性和方法！


```python
b = dir(int) #dir可用来查看属性和方法
b
```




    ['__abs__',
     '__add__',
     '__and__',
     '__bool__',
     '__ceil__',
     '__class__',
     '__delattr__',
     '__dir__',
     '__divmod__',
     '__doc__',
     '__eq__',
     '__float__',
     '__floor__',
     '__floordiv__',
     '__format__',
     '__ge__',
     '__getattribute__',
     '__getnewargs__',
     '__gt__',
     '__hash__',
     '__index__',
     '__init__',
     '__init_subclass__',
     '__int__',
     '__invert__',
     '__le__',
     '__lshift__',
     '__lt__',
     '__mod__',
     '__mul__',
     '__ne__',
     '__neg__',
     '__new__',
     '__or__',
     '__pos__',
     '__pow__',
     '__radd__',
     '__rand__',
     '__rdivmod__',
     '__reduce__',
     '__reduce_ex__',
     '__repr__',
     '__rfloordiv__',
     '__rlshift__',
     '__rmod__',
     '__rmul__',
     '__ror__',
     '__round__',
     '__rpow__',
     '__rrshift__',
     '__rshift__',
     '__rsub__',
     '__rtruediv__',
     '__rxor__',
     '__setattr__',
     '__sizeof__',
     '__str__',
     '__sub__',
     '__subclasshook__',
     '__truediv__',
     '__trunc__',
     '__xor__',
     'bit_length',
     'conjugate',
     'denominator',
     'from_bytes',
     'imag',
     'numerator',
     'real',
     'to_bytes']



这个以后查文档的时候会用到


```python
a = 1101
print(bin(a)) #换成二进制
print(a.bit_length()) #计算二进制长度！
```

    0b10001001101
    11
    


```python
print(1, type(1))

print(1., type(1.))

a = 0.00000023
b = 2.3e-7
print(a) 
print(b)  
```

    1 <class 'int'>
    1.0 <class 'float'>
    2.3e-07
    2.3e-07
    


```python
from decimal import Decimal
```


```python
a = decimal.getcontext() 
print(a)
```

    Context(prec=28, rounding=ROUND_HALF_EVEN, Emin=-999999, Emax=999999, capitals=1, clamp=0, flags=[], traps=[InvalidOperation, DivisionByZero, Overflow])
    
