### 各种匹配模式
注意：正则表达式的匹配要对字符串从头处理到尾，找到所有的共同点，全部表达出来

```py
# \d 数字字符
# \D 非数字字符

# \s 空格字符，包括换行，制表符，空格
# \S 非空格字符

# \w ([a-zA-Z0-9])大小写和数字
# \W 不是上面\w范围中的

# abc 特定字母
# 123 特定数字

# . 任何字符
# \. 匹配.这个字符

# [abc]an 带中括号这一位匹配abc三个字符，an表示后面跟着an，要想全
# [^b]og 带中括号一项表示不匹配b

# [a-z0-6] 表示a-z和0-6
# [^a-z0-6] 表示除了a-z和0-6

# \b 分开单词和非单词的界限（\w+\b）

# 
```

### 出现重复的匹配模式

```py
# \d\d\d 匹配三个数字

# a{3} 匹配a三次

# a{1,3} 一到三次

# 匹配样例
# [wxy]{5}
# .{2,6}
# \d{4,12}

# \d* 0个或任意个数字
# \d+ 1个以上的数字
# a+ 1个以上的a
```

### 匹配可能出现或不出现的字符

```py
# a? 可以有a，也可以没有
# \? 匹配?

# (\d{3})? 判断一种组合是否存在时，要加括号进行分组
```

### 规定匹配的开头和结尾

```py
# ^ 表示开头,和中括号中的使用不同
# $ 表示结尾
# ^...$ 表示匹配中间的内容

```

### 利用正则表达式提取出字符的组

```py
# () ()内的内容尾一组
# ^(IMG\d+\.png)$有后缀；^(IMG\d+)\.png$无后缀  仅提取括号内的内容

import re
m = re.match(r"(\w+) (\w+)", "Isaac Newton, physicist")
m.group(0)       # The entire match
m.group(1)       # The first parenthesized subgroup.
m.group(2)       # The second parenthesized subgroup.
result = m.group(1, 2)    # Multiple arguments give us a tuple.
print(result)
```
运行结果
```py
('Isaac', 'Newton')
```

### 嵌套组的提取

```py
# ^(IMG(\d+))\.png$ 通过上面的group方法，提取不同层次的信息
```

### 有多种选择时的简化

```py
# (milk|bread|juice) 表示三种里面选择一个
```








