# 安装

```bash
brew install python3
```

```bash
// easy_install自带包管理，代替优化版pip(等同node的npm、yarn)
sudo easy_install pip

// 代码校验
sudo pip install flake8

// 格式化
sudo pip install yapf
```

settings.json配置([VSCode的Python插件](https://github.com/DonJayamanne/pythonVSCode))

```js
{
    "python.pythonPath": "python3",
    "python.linting.outputWindow": "python3",
    "python.linting.pylintEnabled": false,
    "python.linting.flake8Enabled": true,
    "python.linting.maxNumberOfProblems": 50,
    "python.formatting.provider": "yapf"
}
```

#命令

CPython 安装完毕自带官方解释器,使用最广

```bash
python3 // 运行3.6+

>>> print('100 + 200 =', 100 + 200) // 逗号 = 空格 + 连字符
100 + 200 = 300

>>> name = input('Please enter your name: ') // 输入
Please enter your name: flyn // 手动输入
>>> print('My name is', name)
My name is 'flyn'

>>> exit() // 退出
```

# 基础

约定俗成最好是4个空格缩进

```bash
# print absolute value of an integer:
a = 100
if a >= 0:
    print(a)
else:
    print(-a)
```

## 数据类型

**整数**

- 十进制 `-9` `-1` `0` `10` `123`
- 十六进制0x为开头 `0xff00` `0xa5b4c3d2`

**浮点数**

- 数学写法，如1.23，3.14，-9.01
- 科学计数法，如1.23x10^9 写成1.23e9，或12.3e8，0.000012可以写成1.2e-5

**字符串**

- `\` 转义字符

```bash
>>> print('I\'m ok.')
I'm ok.
>>> print('I\'m learning\nPython.')
I'm learning
Python.
>>> print('\\\n\\')
\
\
```

- 简易转义，用r''表示''内部的字符串默认不转义

```bash
>>> print('\\\t\\')
\       \
>>> print(r'\\\t\\')
\\\t\\
```

- 简化多个换行情况，用'''...'''的格式表示多行内容

命令行中

```bash
>>> print('''line1
... line2
... line3''')
line1
line2
line3
```

文件中

```
print('''line1
line2
line3''')
line1
line2
line3
```

**布尔值**

True VS False (注意首字母大写)

and or not （运算符：与，或，否）

**空值**

None

**变量**

动态可变

**常量**

简易常量全大写PI，表示不要改变，约定俗成而已

```bash
>>> 10 / 3
3.3333333333333335

<!--整除也还是浮点数-->
>>> 9 / 3
3.0

<!--地板除`//`永远是整数-->
>>> 10 // 3
3

<!--取余数-->
>>> 10 % 3
1
```

## 字符串和编码

`ord()`函数获取字符的整数表示，`chr()`函数把编码转换为对应的字符

```bash
>>> ord('A')
65
>>> ord('中')
20013
>>> chr(66)
'B'
>>> chr(25991)
'文'
```

十六进制写法

```bash
>>> '\u4e2d\u6587'
'中文'
```



