# Python入门萌新避坑指南（1）

# 1 简介

# 2 变量、运算符与数据类型

# 3 位运算

# 4 条件语句

## 1. if 语句


```python
if 2 > 1 and not 2 > 3:
    print('Correct Judgement!')

# Correct Judgement!
```

    Correct Judgement!
    

## 2. if - else 语句


```python
temp = input("猜一猜小姐姐想的是哪个数字？")
guess = int(temp) # input 函数将接收的任何数据类型都默认为 str。
if guess == 666:
    print("你太了解小姐姐的心思了！")
    print("哼，猜对也没有奖励！")
else:
    print("猜错了，小姐姐现在心里想的是666！")
print("游戏结束，不玩儿啦！")
```

    猜一猜小姐姐想的是哪个数字？ 8
    

    猜错了，小姐姐现在心里想的是666！
    游戏结束，不玩儿啦！
    


```python
hi = 6
if hi > 2:
    if hi > 7:
        print('好棒!好棒!')
else:
    print('切~')

# 无输出
```


```python
temp = input("猜一猜小姐姐想的是哪个数字？")
guess = int(temp)
if guess > 8:
    print("大了，大了")
else:
    if guess == 8:
        print("你太了解小姐姐的心思了！")
        print("哼，猜对也没有奖励！")
    else:
        print("小了，小了")
print("游戏结束，不玩儿啦！")
```

    猜一猜小姐姐想的是哪个数字？ 10
    

    大了，大了
    游戏结束，不玩儿啦！
    



## 3. if - elif - else 语句


```python
temp = input('请输入成绩:')
source = int(temp)
if 100 >= source >= 90:
    print('A')
elif 90 > source >= 80:
    print('B')
elif 80 > source >= 60:
    print('C')
elif 60 > source >= 0:
    print('D')
else:
    print('输入错误！')
```

    请输入成绩: 98
    

    A
    

## 4. assert 关键词


```python
my_list = ['lsgogroup']

my_list.pop(0)

assert len(my_list) > 0

# AssertionError
```


    ---------------------------------------------------------------------------

    AssertionError                            Traceback (most recent call last)

    <ipython-input-11-1b40ee6abfb0> in <module>
          3 my_list.pop(0)
          4 
    ----> 5 assert len(my_list) > 0
          6 
          7 # AssertionError
    

    AssertionError: 



```python
assert 3 > 7

# AssertionError
```


    ---------------------------------------------------------------------------

    AssertionError                            Traceback (most recent call last)

    <ipython-input-12-2b14821de816> in <module>
    ----> 1 assert 3 > 7
          2 
          3 # AssertionError
    

    AssertionError: 


# 5 循环语句


```python
count = 0
while count < 3:
    temp = input("猜一猜小姐姐想的是哪个数字？")
    guess = int(temp)
    if guess > 8:
        print("大了，大了")
    else:
        if guess == 8:
            print("你太了解小姐姐的心思了！")
            print("哼，猜对也没有奖励！")
            count = 3
        else:
            print("小了，小了")
    count = count + 1
print("游戏结束，不玩儿啦！")
```

    猜一猜小姐姐想的是哪个数字？ 7
    

    小了，小了
    

    猜一猜小姐姐想的是哪个数字？ 1
    

    小了，小了
    

    猜一猜小姐姐想的是哪个数字？ 1
    

    小了，小了
    游戏结束，不玩儿啦！
    


```python
string = 'abcd'
while string:
    print(string)
    string = string[1:]

# abcd
# bcd
# cd
# d
```

    abcd
    bcd
    cd
    d
    


```python
count = 0
while count < 5:
    print("%d is  less than 5" % count)
    count = count + 1
else:
    print("%d is not less than 5" % count)
    
# 0 is  less than 5
# 1 is  less than 5
# 2 is  less than 5
# 3 is  less than 5
# 4 is  less than 5
# 5 is not less than 5
```

    0 is  less than 5
    1 is  less than 5
    2 is  less than 5
    3 is  less than 5
    4 is  less than 5
    5 is not less than 5
    


```python
count = 0
while count < 5:
    print("%d is  less than 5" % count)
    count = 6
    break
else:
    print("%d is not less than 5" % count)

# 0 is  less than 5
```

    0 is  less than 5
    

## 3. for 循环


```python
for i in 'ILoveLSGO':
    print(i, end=' ')  # 不换行输出

# I L o v e L S G O
```

    I L o v e L S G O 


```python
member = ['张三', '李四', '刘德华', '刘六', '周润发']
for each in member:
    print(each)

# 张三
# 李四
# 刘德华
# 刘六
# 周润发

for i in range(len(member)):
    print(member[i])

# 张三
# 李四
# 刘德华
# 刘六
# 周润发
```

    张三
    李四
    刘德华
    刘六
    周润发
    张三
    李四
    刘德华
    刘六
    周润发
    


```python
dic = {'a': 1, 'b': 2, 'c': 3, 'd': 4}

for key, value in dic.items():
    print(key, value, sep=':', end=' ')
    
# a:1 b:2 c:3 d:4 
```

    a:1 b:2 c:3 d:4 


```python
dic = {'a': 1, 'b': 2, 'c': 3, 'd': 4}

for key in dic.keys():
    print(key, end=' ')
    
# a b c d 
```

    a b c d 


```python
dic = {'a': 1, 'b': 2, 'c': 3, 'd': 4}

for value in dic.values():
    print(value, end=' ')
    
# 1 2 3 4

```

    1 2 3 4 

## 4. for - else 循环


```python
for num in range(10, 20):  # 迭代 10 到 20 之间的数字
    for i in range(2, num):  # 根据因子迭代
        if num % i == 0:  # 确定第一个因子
            j = num / i  # 计算第二个因子
            print('%d 等于 %d * %d' % (num, i, j))
            break  # 跳出当前循环
    else:  # 循环的 else 部分
        print(num, '是一个质数')

# 10 等于 2 * 5
# 11 是一个质数
# 12 等于 2 * 6
# 13 是一个质数
# 14 等于 2 * 7
# 15 等于 3 * 5
# 16 等于 2 * 8
# 17 是一个质数
# 18 等于 2 * 9
# 19 是一个质数
```

    10 等于 2 * 5
    11 是一个质数
    12 等于 2 * 6
    13 是一个质数
    14 等于 2 * 7
    15 等于 3 * 5
    16 等于 2 * 8
    17 是一个质数
    18 等于 2 * 9
    19 是一个质数
    


```python
for i in range(2, 9):  # 不包含9
    print(i)

# 2
# 3
# 4
# 5
# 6
# 7
# 8
```

    2
    3
    4
    5
    6
    7
    8
    


```python
for i in range(1, 10, 2):
    print(i)

# 1
# 3
# 5
# 7
# 9
```

    1
    3
    5
    7
    9
    


```python
seasons = ['Spring', 'Summer', 'Fall', 'Winter']
lst = list(enumerate(seasons))
print(lst)
# [(0, 'Spring'), (1, 'Summer'), (2, 'Fall'), (3, 'Winter')]
lst = list(enumerate(seasons, start=1))  # 下标从 1 开始
print(lst)
# [(1, 'Spring'), (2, 'Summer'), (3, 'Fall'), (4, 'Winter')]
```

    [(0, 'Spring'), (1, 'Summer'), (2, 'Fall'), (3, 'Winter')]
    [(1, 'Spring'), (2, 'Summer'), (3, 'Fall'), (4, 'Winter')]
    


```python
languages = ['Python', 'R', 'Matlab', 'C++']
for language in languages:
    print('I love', language)
print('Done!')
# I love Python
# I love R
# I love Matlab
# I love C++
# Done!


for i, language in enumerate(languages, 2):
    print(i, 'I love', language)
print('Done!')
# 2 I love Python
# 3 I love R
# 4 I love Matlab
# 5 I love C++
# Done!
```

    I love Python
    I love R
    I love Matlab
    I love C++
    Done!
    2 I love Python
    3 I love R
    4 I love Matlab
    5 I love C++
    Done!
    


```python
import random
secret = random.randint(1, 10) #[1,10]之间的随机数

while True:
    temp = input("猜一猜小姐姐想的是哪个数字？")
    guess = int(temp)
    if guess > secret:
        print("大了，大了")
    else:
        if guess == secret:
            print("你太了解小姐姐的心思了！")
            print("哼，猜对也没有奖励！")
            break
        else:
            print("小了，小了")
print("游戏结束，不玩儿啦！")
```

    猜一猜小姐姐想的是哪个数字？ 8
    

    大了，大了
    

    猜一猜小姐姐想的是哪个数字？ 0
    

    小了，小了
    

    猜一猜小姐姐想的是哪个数字？ 5
    

    你太了解小姐姐的心思了！
    哼，猜对也没有奖励！
    游戏结束，不玩儿啦！
    


```python
for i in range(10):
    if i % 2 != 0:
        print(i)
        continue
    i += 2
    print(i)

# 2
# 1
# 4
# 3
# 6
# 5
# 8
# 7
# 10
# 9
```

    2
    1
    4
    3
    6
    5
    8
    7
    10
    9
    

# 6 异常处理


```python

```
