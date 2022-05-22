## UCB CS61A Fall 2020 Note

### Lecture2

#### Defining Functions

##### Abstraction

Assignment is a simple means of abstraction: binds names to values 

Function definition is a more powerful means of abstraction: binds names to expressions

> Abstraction is the process of taking something complex, giving it a name, and **treating it as a whole without worrying about all of its details**.

### Lab1

#### Boolean Operators

##### Short Circuiting

Short-circuiting happens when the operator reaches an operand that allows them to make a conclusion about the expression. For example, `and` will short-circuit as soon as it reaches the first false value because it then knows that not all the values are true.

If `and` and `or` do not *short-circuit*, they just return the last value; another way to remember this is that **`and` and `or` always return the last thing they evaluate, whether they short circuit or not.** 

```python
# False: False 0 '' None
>>> True and 0
0
>>> 0 and True
0 # short-circuit
>>> False or 0
0
>>> 0 or False
False
>>> 1 or False
1 # short-circuit

>>> 1 and 3 and 6 and 10 and 15
15
```

Keep in mind that `and` and `or` **don't always return booleans when using values other than `True` and `False`.**

```python
>>> -1 and 1 > 0
True # -1 and 1 -> 1 ---> 1 > 0 -> True
>>> 0 or False or 2 or 1 / 0
2 # 0 or False -> False ---> False or 2 -> 2
```

### Lecture4

#### Designing Functions

Give each function exactly **one job**, but make it apply to many related situations.

**Don’t repeat yourself** (DRY).

- Implement a process just once, but execute it many times.

Define functions **generally**.

- Generalizing Patterns with Arguments

  ![](https://image-for-robins-blog.oss-cn-shanghai.aliyuncs.com/img/image-20220516112712073.png)

- Generalizing Over Computational Processes

  ![](https://image-for-robins-blog.oss-cn-shanghai.aliyuncs.com/img/image-20220516120657296.png)

#### Control

##### If Statements and Call Expressions

Why the Python programming language has a separate kind of statement for conditionals instead of just using another function, that's because **functions always evaluate their components** but control statements skip some parts or repeat some parts and that's just not something that call expressions can do.

![](https://image-for-robins-blog.oss-cn-shanghai.aliyuncs.com/img/image-20220516220833098.png)

![](https://image-for-robins-blog.oss-cn-shanghai.aliyuncs.com/img/image-20220516221005114.png)