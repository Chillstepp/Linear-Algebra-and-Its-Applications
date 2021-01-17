---
title: 《线性代数及其应用》CH2：矩阵代数
date: 2021-01-17 20:20:31
tags: 线性代数
---

# 第二章  矩阵代数

## 2.1 矩阵运算

**对角矩阵，零矩阵定义：**

![image-20210116150748619](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210116150748619.png)

**矩阵与标量的乘法：**

![image-20210116151001880](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210116151001880.png)

**一些矩阵乘法的相关性质：**

![image-20210116153840948](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210116153840948.png)

**矩阵转置：**

![image-20210116154805235](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210116154805235.png)

**转置的相关性质：**

![image-20210116154834116](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210116154834116.png)

前三个很简单，最后一个证明从定义入手：

![image-20210116155736051](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210116155736051.png)

## 2.2 矩阵的逆

**矩阵可逆：**

![image-20210116160937237](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210116160937237.png)



- 不可逆矩阵 = 奇异矩阵
- 可逆矩阵 = 废弃及矩阵

**判断矩阵是否可逆：**

![image-20210116161301492](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210116161301492.png)



**方程唯一解 与 矩阵可逆：**

![image-20210116161736676](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210116161736676.png)



![image-20210116162136500](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210116162136500.png)

![image-20210116172308887](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210116172308887.png)

c.证明：

![image-20210117135038734](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210117135038734.png)



**初等变换 的等价:**

对于一个单位矩阵$I$, 我们进行初等变换为 $I$’, 然后再和 矩阵$E$ 相乘 等于$I'E$, 这个等价于直接对$E$做同样的初等变换。

例如：把单位矩阵的第一行的-4倍加到第3行，得到：

![image-20210117140601553](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210117140601553.png)

![image-20210117140729134](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210117140729134.png)

然后再和矩阵A相乘得：

![image-20210117140706336](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210117140706336.png)

我们观察这个矩阵其实和A直接做初等变换是一样的，都是第一行的-4倍加到第3行。



这个性质可以求逆：

![image-20210117142106096](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210117142106096.png)

我们想让$E_1$ 乘一个矩阵边为单位矩阵，那么可以让矩阵为 第一行的+4倍加到第三行就变成了单位矩阵了，这可以利用上面那个性质。

![image-20210117142240873](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210117142240873.png)

这个矩阵相当于对单位矩阵做了第一行的+4倍加到第三行的初等变化，那么乘上$E_1$ 就相当于$E_1$做了 初等变化（第一行的+4倍加到第三行的初等变化），从而变成了单位矩阵，那么$E_1$ 的逆就是 ![image-20210117142240873](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210117142240873.png)

这也就对应上了这个定理：

![image-20210117142523157](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210117142523157.png)

简单理解就是一个矩阵如果可以经过初等变换变成单位矩阵，那么他就有逆，且他的逆就是 单位矩阵乘上那些初等变化矩阵。



因此我们此时就可以提出**求矩阵逆的算法**：

![image-20210117143114850](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210117143114850.png)



这个很好理解，还是上边的意思，只不过通过矩阵这种形式化的数学语言做了简要概述，对于一个矩阵A，我通过初等变化变为了单位矩阵，说明对单位矩阵做同样的操作，这个就是A的逆矩阵，



求矩阵逆的算法的例题：

![image-20210117143414963](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210117143414963.png)



## 2.3 可逆矩阵的特征

![image-20210117144434093](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210117144434093.png)

证明上述定理只需要证明下述的这个环即可：

![image-20210117144627136](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210117144627136.png)



## 2.4 分块矩阵

首先是一些基本计算和普通矩阵是没有区别的。



**分块矩阵基本运算：**

![image-20210117150748185](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210117150748185.png)



**分块矩阵的逆：**

![image-20210117150928379](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210117150928379.png)

不妨设：

![image-20210117151423411](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210117151423411.png)

列出方程：

![image-20210117151458449](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210117151458449.png)

得到：

![image-20210117162850944](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210117162850944.png)



知道怎么来的即可，分块求逆有很多公式，对应着不同的情况。



## 2.5 矩阵因式分解

**LU分解：**

对于这样的一个问题

![image-20210117165207504](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210117165207504.png)

我们可以一个一个的求解。

当然，如果A可逆，也可以先算$A^{-1}$, 然后直接算$x = A^{-1}b$,即可算出解。



![image-20210117165532065](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210117165532065.png)

![image-20210117173317201](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210117173317201.png)

我们首先可以解$Ly=b$ 这个方程得出$y$,然后算 $Ux=y$ , 解出$x$, 同时我们注意到由于L,U都是三角矩阵，很容易就可以解出来方程。



**LU分解算法：**

![image-20210117173706927](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210117173706927.png)

![image-20210117174212590](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210117174212590.png)

![image-20210117175213667](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210117175213667.png)

![image-20210117174520420](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210117174520420.png)

L的计算方法很简单，我们在上述将A变成阶梯型矩阵U的过程中，我们就是把每一列

![image-20210117175235905](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210117175235905.png)



## 2.7 计算机图形学

这个在博文《AHU计算机图形学》有详细的解释



## 2.8 $R^n$的子空间

![image-20210117181653194](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210117181653194.png)



![image-20210117182335539](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210117182335539.png)



**矩阵的列空间：**

![image-20210117182500074](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210117182500074.png)

![image-20210117182654579](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210117182654579.png)





![image-20210117184509730](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210117184509730.png)



**矩阵的零空间：**

![image-20210117190707869](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210117190707869.png)

![image-20210117191117534](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210117191117534.png)



**子空间的基：**

![image-20210117191239270](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210117191239270.png)

标准基

![image-20210117191307369](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210117191307369.png)

![image-20210117192242118](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210117192242118.png)

![image-20210117192259496](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210117192259496.png)

![image-20210117193137910](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210117193137910.png)

零空间Null A 其实是保证了它一定是矩阵的基。



![image-20210117193343288](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210117193343288.png)

我们可以直接找主元列作为列空间的基，即下面这个定理：

![image-20210117193535647](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210117193535647.png)

![image-20210117193745935](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210117193745935.png)

![image-20210117193729487](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210117193729487.png)



## 2.9 维数与秩



![image-20210117194910951](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210117194910951.png)



![image-20210117195406233](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210117195406233.png)

![image-20210117195342734](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210117195342734.png)

**矩阵的秩：**

![image-20210117195552448](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210117195552448.png)

我们一般称子空间的维数为秩：

![image-20210117195644510](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210117195644510.png)



![image-20210117200557919](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210117200557919.png)

![image-20210117201744608](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210117201744608.png)

**秩与可逆矩阵定理 ：**

![image-20210117201538673](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210117201538673.png)

