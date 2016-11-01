## 用Javascript编写一个编译器

在布鲁克林 布什威克的一个美好的星期天，我在本地书店发现了一本John Maeda写的“数字设计”的书，这本书里一步一步的教DBN编程语言--一种90年代末在麻省理工学院媒体实验室诞生的语言，旨在以可视化的方式介绍计算机编程概念。

我迫切地想让SVG来实现DBN并运行它在浏览器在2016年将是一个有趣的项目,而不是安装Java环境执行原始DBN源代码。

我想我需要些一个DBN到SVG的编译器，所以编写一个编译器的任务已经开始。 “写一个编译器”听起来像很多计算机科学...但我从来没有接触过这方面，我可以写一个编译器吗？

### 让我们先试着做一个编译器

编译器是一种采用一段代码并将其转换为其他代码的机制。 让我们将简单的DBN代码编译成一个物理图。

在这个DBN代码中有3个命令，“Paper”定义纸张的颜色，“Pen”定义笔的颜色，“Line”画一条线。 颜色参数100表示CSS中的100％黑色或rgb（0％，0％，0％）。 在DBN中产生的图像总是灰度的。 在DBN中，纸张始终为100×100，线宽始终为1，并且线由起点的x y坐标和从左下角计数的终止点定义。

让我们试着成为一个编译器自己。 停在这里，抓住一张纸和一支钢笔，尝试编译以下代码作为绘图。

```js
Paper 0
Pen 100
Line 0 50 100 50
```