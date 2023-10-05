# Latex公式简要笔记

## 概述

在研究和表达一些游戏中使用到的基础数学时，我们便会遇到数学公式书写和显示的问题。虽然用绘图工具手写也没啥毛病，但是终究有点费力，且不优雅。

LaTeX是一个基于宏标记语言的排版系统，可以简单理解为MarkDown的复杂版本。LaTeX解决了复杂数学公式的排版问题，而目前主流的MarkDown编辑器，都支持了LaTeX数学公式的书写和显示支持。

LaTeX使用`\指令`形式控制排版的元素，你可以简单的将LaTeX指令当做是函数，而LaTeX公式的表达式是在书写某种形式的脚本。

用LaTeX格式书写数学公式，一个是标准（至少以学术要求来说），一个是美观（自动、标准化排版）。

而且基本上日常使用，尤其是游戏方面，记住三五个到十来个写法就完全够用了。

本篇就是基于日常游戏相关的简单四则运算，平方，开方，三角函数，向量、矩阵所能用到的数学公式所做的浓缩。

### 参考视频

[【Latex公式教程】 教你用Typora解决99%的数学公式输入难题_哔哩哔哩_bilibili](https://www.bilibili.com/video/BV1NT411C7wS/?spm_id_from=333.337.search-card.all.click&vd_source=2f49ad1693bc7945c7bf165c74c86263)

### 说明

- 在最新版（1.7.5）Typora中不支持`$公式$`形式的行内公式（或者是因为我是试用版？），而VScode支持。

- 在语雀中需要使用`\`指令调出“公式”，来插入LaTeX公式。而且不需要输入`$`或`$$`。
- 在Typora、VScode以及语雀中国，LaTeX数学公式的语法是一致的。
- 

## 上下标

上下标是最常见也最常用的。

- `_下标`或`_{下标}`
- `^上标`或`^{上标}`
- 上标或下标的顺序可以颠倒

```latex
$$
x_2^5+y^5_4
$$
```

$$
x_2^5+y^5_4
$$

复杂的上下标需要使用`{}`括住上下标的内容。

```latex
$$
x_2^{5+i}+y^5_{4-k}
$$
```


$$
x_2^{5+i}+y^5_{4-k}
$$

还可以使用`\sideset`进行四个位置的上下标设定。

```latex
$$
\sideset{_1^2}{_3^4}A
$$
```


$$
\sideset{_1^2}{_3^4}A
$$


## 三角函数
基本上就是原样写就行，度数可以使用`°`，但是并不标准，标准写法是使用`\degree`。
```latex
$$
sin(30\degree)+cos(45\degree)
$$
```

$$
sin(30\degree) + cos(45\degree)
$$

## 乘法

乘法符号包括最常见的×号，以及点乘符号。

### 乘法

×号用`\times`就可以。

```
$$
a \times b
$$
```
$$
a \times b
$$

### 点乘

点乘可以使用`\cdot`。

```latex
$$
A \cdot B
$$
```
$$
A \cdot B
$$

## 除法

### 标准除法符号

标准的除法符号可以使用`num1 \div num2`形式。

```latex
$$
a \div b
$$
```

$$
a \div b
$$

或者也可以采用`除数/被除数`形式。
$$
a/b
$$

### 分数形式

分数，单词`fraction`，指令形式为`\frac{分子}{分母}`。

```latex
$$
\frac{1}{2} +\frac{a+b}{c^2}
$$
```
$$
\frac{1}{2} +\frac{a+b}{c^2}
$$

## 开方

开方也比较常用,平方根英文`square root`,LateX指令`\sqrt[开方次数]{底}`，默认可以不写开方次数，只写底，则默认为开平方根。

```latex
$$
\sqrt{a^2+b^2}
$$
```
$$
\sqrt{a^2+b^2}
$$
或者：
```latex
$$
\sqrt[3]{2}
$$
```
$$
\sqrt[3]{2}
$$

## 省略
`\dots`是最简单的，用于表示省略。

```latex
$$
a+b+c \dots + n
$$
```


$$
a+b+c \dots + n
$$
## 向量
最简形式：`\vec{向量名}`。
```latex
$$
\vec{a} - \vec{b} = \vec{a} + (-\vec{b})
$$
```


$$
\vec{a} - \vec{b} = \vec{a} + (-\vec{b})
$$

## 累加

累加或者叫求和，指令`\sum`,可以跟上上下标，通常的写法就是`\sum_{i=起始}^{结束}i的表达式`，表示i=起始到结束，对i的表达式进行累加求和。

```latex
$$
\sum_{i=1}^{10}i^2 = 1^2 +2^2+\dots+ 10^2
$$
```


$$
\sum_{i=1}^{10}i^2 = 1^2 +2^2+\dots+ 10^2
$$

上面的公式就是对表达式i的平方进行i=1到10的累加运算。

## 累乘

累乘和累加类似。只不过符号发生了变化。

```latex
$$
\prod_{i=1}^{10}i = 1 \times 2 \times \dots \times 10
$$
```

$$
\prod_{i=1}^{10}i = 1 \times 2 \times \dots \times 10
$$

## 希腊字母

记住最常用的αβγπ就够用了，实在需要的时候百度一下。

```latex
$$
\alpha + \beta + \gamma + \pi
$$
```
$$
\alpha + \beta + \gamma + \pi
$$
```latex
$$
\Alpha + \Beta + \Gamma + \Pi 
$$
```
$$
\Alpha + \Beta + \Gamma + \Pi 
$$

## 特殊符号



```latex
$$
\ge \le \ll \neq \geqslant \leqslant \approx
$$
```
$$
\ge \le \ll \neq \geqslant \leqslant \approx
$$

## 颜色
```latex
$$
\color{red}{A}
$$
```


$$
\color{red}{A}
$$

## 矩阵
```latex
$$
\begin{matrix}
1 & 0 & 0\\
0 & 1 & 0\\
0 & 0 & 1\\
\end{matrix}
$$
```



$$
\begin{matrix}
1 & 0 & 0\\
0 & 1 & 0\\
0 & 0 & 1\\
\end{matrix}
$$


```latex
$$
\begin{bmatrix}
1 & 0 & 0\\
0 & 1 & 0\\
0 & 0 & 1\\
\end{bmatrix}
$$
```

$$
\begin{bmatrix}
1 & 0 & 0\\
0 & 1 & 0\\
0 & 0 & 1\\
\end{bmatrix}
$$

```latex
$$
\begin{vmatrix}
1 & 0 & 0\\
0 & 1 & 0\\
0 & 0 & 1\\
\end{vmatrix}
$$
```


$$
\begin{vmatrix}
1 & 0 & 0\\
0 & 1 & 0\\
0 & 0 & 1\\
\end{vmatrix}
$$