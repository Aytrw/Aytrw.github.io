---
title: tarjan算法
date: 2018-08-13 14:44:58
tags: 数据结构
categories: 图论
---
>tarjan算法是一种求解有向图强连通分量的线性时间的算法
为了了解tarjan算法，我们先需要了解以下几个概念<!-- more -->

# 引入概念
强连通(Strongly Connected)：
<div class="note info"><p>在一张有向图G中，设a，b∈G，且a有一条路可以走到b，而b也可以走到a
</p></div>强连通图(Strongly Connected Graph)：
<div class="note info"><p>在一张有向图G中，∀a，b∈G都强连通
</p></div>强连通分量(Strongly Connected Components)：
<div class="note info"><p>在一张有向图G中，有一张子图H，且∀a，b∈H都强连通
我们就将H称为强连通分量</p></div>
下面我将给出一个具体的例子：
![1](tarjan算法/pic.png)给定如图所示的一张有向图
在这张有向图中，我们可以看到由结点1，3，4，5构成的子图中
任意两个顶点都是强连通的，因此，这张子图就是他的强连通分量

# 算法详解
Tarjan算法是基于DFS的算法，每个`强连通分量`都是`搜索树`中的一棵`子树`
对于这一张有向图来说，就是一棵`完整的搜索树`
为了方便操作，我们将每个点设置两个参数
1.DFN[i]，表示这个点搜索的次序编号(时间戳)
<div class="note info">时间戳：表示第几个被搜索到的，每个点的时间戳都不一样<p></p></div>
2.LOW[i]，作为每个点在这棵树中最小子树的根
我们选用`堆栈`来储存整个强连通分量，如果有新结点就进栈，如果该点有出度就继续找

未完待续。


<div class="note warning">本文仅供学习参考之用，转载请注明作者
本文只是作者个人理解，如有错误在此将表示歉意，并欢迎指出
<p></p></div>