---
title: 《线性代数及其应用》CH1：线性代数中的线性方程组
date: 2021-01-13 13:00:46
tags: 线性代数
---



[TOC]

# 第1章 线性代数中的线性方程组

## 1.1 线性方程组



![image-20210112120520806](https://i.loli.net/2021/01/12/zxe5JKMqT8yC6Eu.png)



线性方程的解有三种情况

- 无解
- 唯一解
- 无穷多解

当方程组有解，我们称线性方程组是**相容的**。反之无解称之为**不相容的**。



![image-20210112121306672](https://i.loli.net/2021/01/12/TYgD2c7usqd43Z9.png)

我们称 ![image-20210112121548970](https://i.loli.net/2021/01/12/uIA3WsgNU9PTDnS.png)为**系数矩阵**，称![image-20210112121629863](https://i.loli.net/2021/01/12/5pzNnmxLWdElbQo.png)为**增广矩阵**。

解方程的方法：我们可以通过变换先变成![image-20210112122354570](https://i.loli.net/2021/01/12/XCAOVI1L6U3onRD.png)

然后通过第三行消去第二行的$x_3$，然后用只包含$x_2$的第二行和只包含$x_3$的第三行消去第一行的$x_2$和$x_3$

最后得到：

![image-20210112122535424](https://i.loli.net/2021/01/12/4xaVRu8EX6ArefS.png)

![image-20210112122612697](https://i.loli.net/2021/01/12/6G87WdMkcZOlxfi.png)

直观理解就是三个平面交于一点，这也是线性方程组的几何意义。



**初等变换**主要有三种：

- 倍加：把某一行可以以某个倍数加到另一行上
- 对换：把两行对换
- 倍乘：把某一行的所有元素乘以同一个非零数



![image-20210112123403474](https://i.loli.net/2021/01/12/hn6tZGolMkN1cYP.png)

我们通过进行如上提到的变换可以得到：

![image-20210112123421283](https://i.loli.net/2021/01/12/lbH9mwknKsY87TL.png)



## 1.2 行化简与阶梯形矩阵

**阶梯型矩阵：**

![image-20210112143300127](https://i.loli.net/2021/01/12/gilsFd2cUBQItGb.png)

其实就是下面这样的矩阵：

![image-20210112143334007](https://i.loli.net/2021/01/12/zFL69amXbTCJlMs.png)



**化简阶梯矩阵：**

![image-20210112145222102](https://i.loli.net/2021/01/12/AhGbgX6dItFfQOD.png)



**定理1： 每个矩阵等价于唯一的化简阶梯形矩阵**



![image-20210112144420086](https://i.loli.net/2021/01/12/DqHjUc7m6yzMp5R.png)

举个例子来说明一下主元位置和主元列的具体意义：

![image-20210112144521767](https://i.loli.net/2021/01/12/nmQwGoTtJi6yX9z.png)

例如上图，我们首先化简为阶梯型

![image-20210112144641912](https://i.loli.net/2021/01/12/AJ9K8FcdvhIRQxS.png)

观察上图不难理解主元列就是主元位置所在的列，主元位置就是每行第一个非0的元素所在的位置。





![image-20210112151652307](https://i.loli.net/2021/01/12/TejwAz1uYpf6MOB.png)

![image-20210112153514849](https://i.loli.net/2021/01/12/lTedBGrxhoD5smZ.png)



同理：

![image-20210112153942409](https://i.loli.net/2021/01/12/CxntVEDZK7maR8I.png)



**存在与唯一性定理：**

![image-20210112154346769](https://i.loli.net/2021/01/12/zTQOvP7SaAHkmcx.png)



![image-20210112154655355](https://i.loli.net/2021/01/12/w9zqsfhRt5MkWTB.png)



## 1.3 向量方程

**定义：**

![image-20210112155216842](https://i.loli.net/2021/01/12/eh4HRLs1IpMSvnZ.png)

![image-20210112155256513](https://i.loli.net/2021/01/12/HeuVmELOzjysNa8.png)



**几何表示：**

![image-20210112155428557](https://i.loli.net/2021/01/12/UQ1IpXdBRyNMKxL.png)



同理$R^3$中的3*1的矩阵可以看作**立体空间中的向量**。

不难发现可以推广到$R^3$

![image-20210112160252410](https://i.loli.net/2021/01/12/JgRlLVK5QyoBS9b.png)

线性组合其实本质也是解方程组问题，如下：

![image-20210112160640059](https://i.loli.net/2021/01/12/7Gx6hYFac8I39Vb.png)

![image-20210112160713322](https://i.loli.net/2021/01/12/vzTymN6co5deODp.png)



定义：向量组张成的空间中的子集

![image-20210112161041658](https://i.loli.net/2021/01/12/wKdtGaxh4yzrpbE.png)



因此我们判断一个向量是否属于$Span\{v_1,v_2,v_3...,v_p\}$,我们只需要判断

​	$x_1v_1+x_2v_2+x_3v_3...x_pv_p=b$  是否有解即可。



不难理解$Span\{v_1\}$就是一条线 ，$Span\{v_1，v_2\}$就成为了一个二维平面（当然前提$v_1,v_2$方向即不是相同同，也不是相反，因为符合该条件的两个向量本质是一个方向的东西，并不能张成一个二维平面）



## 1.4 矩阵方程$Ax = b$

![image-20210112162048243](https://i.loli.net/2021/01/12/SC8DX6JPcrR4Et2.png)

以下四个定义不难理解是等价的：

![image-20210112180444746](https://i.loli.net/2021/01/12/czRWEpLxlNM5PwT.png)

注意：定理四所提到的等价是**A为系数矩阵**的情况下，若为增广矩阵$[A\  b]$,则不一定适合，比如若增广矩阵最后一行为  [0 0 0 ... 0 4] 那么显然最后一行是有主元的，但是这个方程肯定是无解的，因为 0*x不可能等于4。



**Ax的计算方法：**  本质就是矩阵乘法的一种特殊情况

![image-20210112181316398](https://i.loli.net/2021/01/12/H58VgxDn42ePmGF.png)



**一些显而易见的结论：**

![image-20210112181516999](https://i.loli.net/2021/01/12/9fnXwUcNgbGKLoJ.png)



## 1.5 线性方程组的解集

**齐次线性方程组：**

[![sYev59.png](https://s3.ax1x.com/2021/01/12/sYev59.png)](https://imgchr.com/i/sYev59)



![image-20210112183931424](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210112183931424.png)

上面这句话很好理解，如果没有自由变量就说明解就只有一个，也就是说这一个解肯定是那个全为0的平凡解。



![image-20210112184834628](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210112184834628.png)



![image-20210112184906243](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210112184906243.png)

因此$Ax=0$的每一个解都是$v$的倍数。



同理：

![image-20210112185053698](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210112185053698.png)

![image-20210113000915728](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210113000915728.png)



对于这样一个解空间： 

![image-20210113001547590](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210113001547590.png)

我们不难发现这个$x$可以看作 $p$ 的位移，如下图：

![image-20210113001646589](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210113001646589.png)



![image-20210113001823484](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210113001823484.png)

我们不难发现，如果是$Ax=0$, 那么 p这一项消失了就会，但是由于$tv$并不会改变，所以平面方向是不会变的，两个解平面应该是平行的。

注意 : 当然我们上面所讨论的一切建立于方程$Ax=0$至少有一个非零解，我们拆成两部分来看这个非零解：

- 首先肯定是不能无解的，如果是无解就没有解平面了。
- 再看非零这个约束，非零是防止$Ax=0$中出现了平凡解，平凡解没有什么意义，因为$Ax=0$所构造的超平面一定是过原点的。



## 1.6 线性方程组的应用

这也是体现了本书的特点Application的一章。

以化学方程式配平为例：

![image-20210113002811439](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210113002811439.png)

这里就不写太多了，都是一些线性代数中线性方程组的application



## 1.7 线性无关

![image-20210113003038478](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210113003038478.png)

![image-20210113004043615](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210113004043615.png)

![image-20210113004051471](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210113004051471.png)

第一问很简单，我们扔进$Ax=0$看看有没有解即可，即增广矩阵变换一下算出解即可。

b.  因为$x_3$为自由变量，直接随便带入一个即可。



![image-20210113012248277](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210113012248277.png)

两个2维向量a,b构成的向量组线性相关的几何意义是: a,b共线
三个3维向量a,b,c构成的向量组线性相关的几何意义是: a,b,c共面/a,b,c共线

不难发现：  **n个向量所张成的空间维度小于n，那么这n个向量就是线性相关的。**



也就是说：

![image-20210113012923541](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210113012923541.png)

​	其实不难理解，为什么n个向量所张成的空间维度小于n呢？因为有些向量是“假的”，它可以通过其它来的向量来表示，也就是说这个向量可有可无，这样n个向量就会变成n-1，张成空间的维度显然会下降。



**一个显而易见的定理：**

![image-20210113013506696](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210113013506696.png)

直观理解就是一个零向量其实是可有可无的，因此维度自然会下降，因此n个向量所张成的空间维度小于n，那么这n个向量就是线性相关的。



![image-20210113015916689](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210113015916689.png)

这个定理通过构造达到了线性相关的定义，本质还是如下定理：

![image-20210113012923541](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210113012923541.png)





## 1.8 线性变换介绍



![image-20210113020518364](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210113020518364.png)

![image-20210113020532379](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210113020532379.png)

![image-20210113020713436](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210113020713436.png)



我们看一个几何意义：

![image-20210113021209341](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210113021209341.png)

这个也属于计算机图形学的矩阵变换的内容。



**线性变换：**

![image-20210113021406867](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210113021406867.png)

推论：

![image-20210113021447482](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210113021447482.png)



图像旋转（同样属于计算机图形学的内容）：

![image-20210113021551909](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210113021551909.png)



## 1.9 线性变换的矩阵

![image-20210113123134529](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210113123134529.png)



![image-20210113123439184](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210113123439184.png)





**$R^2$中的几何线性变换**



![image-20210113123607215](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210113123607215.png)

![image-20210113123649037](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210113123649037.png)

![image-20210113123709236](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210113123709236.png)

![image-20210113123717581](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210113123717581.png)

![image-20210113123725208](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210113123725208.png)





![image-20210113130357545](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210113130357545.png)



**总结一下：**

这一小节一直在讲映射的问题，其实也是一个降维的问题，比如A 是一个3\*4的矩阵，x是一个4\*1的矩阵，Ax变换后成为了3*1的向量，这是一个降维的过程。但是者可以称之为一个很好的降维方法吗？如果多个4维向量都映射到了同一个三维向量，那么这种不是一对一的映射（单射）是不够优秀的，因此比如：![image-20210113131535375](https://gitee.com/Chillstep/ChillstepPictures/raw/master/master/image-20210113131535375.png)

这个矩阵是有自由变元的，也就是说$Ax=b$ 时，一个b会因为自由变元使得多个x都映射在b上。



