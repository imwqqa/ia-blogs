---
title: '数学分析 - Dedekind 分割与实数系统'
date: 2025-10-05T00:41:07+08:00
categories: [mathematics]
tags: []
summary: 本文从实数的引入开始，在有理数上 Dedekind 分割定义实数系，并由此进一步证明确界存在原理，尝试用不同的视角理解完备性。
draft: false
isCJKLanguage: true
---
{{< katex >}}

数学分析的讨论是基于 \\(\mathbb{R}\\) 的，定义它是一切讨论的基础。

Dedekind 分割视角下，可以理解到任何 \\(r \in \mathbb{R}\\)，即任何实数都代表了一个集合，用这样的方法可以进一步的使用理性理解极限，从而避免依赖直觉产生的似是而非的混乱。

同时，Dedekind 分割展示了将动态迫近的过程转化为集合的精彩方法，并由此自然的延申串联起了集合论与点集拓扑等理论。

## 实数的引入

具体来看，实数的引入的驱动力是来自于实际问题中发现了无法表示的对象。

无理数中的一部分，表示形如 \\(\sqrt{2}\\) 这种对象并不困难。这样的无理数是在解方程中发现的。

考虑 \\(\sqrt{2}\\)，实际上就是由方程 \\(x^2=2\\) 定义出来的，理解它们是比较直观的，虽然无法直接描述，但通过将所有有理系数的多项式构成的方程可以得到的根作为集合，可以将所有这类无理数表示出来，即 \\(\overline{\mathbb{Q}}\\)，代数数。

如果仅是代数数，则没有引入 \\(\mathbb{R}\\) 的必要。

然而，在实际场景中，有另一类无理数更难以被表示，形如 \\(\pi\\), \\(e\\)，它们的特征是可以不断近似，但无法穷尽。同时，它们也不是任何代数方程的根，称为超越数。

这里的核心矛盾是，我们希望有一个迫近的终点，因为终点是静止的，静止、恒常就是确定性；而无法穷尽则代表动态，想要精确就需要不断的运算，动态、变化就是不确定性。

更严峻的是，基于后来的认识，即基数（势）的比较，几乎所有实数都是超越数。

至此，已经明晰了引入全新形式的数，即后来为人所知的实数，来解决表示超越数的问题是必要的。

## 实数的定义

如果与代数数相同，既然代数数是在解方程中发现的，用有理系数多项式的方程的根来定义，那么超越数是否也可以沿用相同的思路，直接通过迫近超越数的过程本身来定义？

Dedekind 分割构造 \\(\mathbb{R}\\) 正是建立在这一思路上的定义方法。

在介绍 Dedekind 分割之前，首先介绍划分这个前置概念。

$$
    \text{Definition (Partition):} \\\\[1ex]
    \text{A partition of a set } A \text{, is a pair of disjoint subsets } \(\alpha,\ \beta\) \text{ such that: } \\\\[0.8ex]
    \begin{aligned}
        &\text{1. } \alpha \cup \beta = A.\\\\
        &\text{2. } \alpha \cap \beta = \varnothing.
    \end{aligned}
$$

划分是一对是任意集合 \\(A\\) 的子集 \\(\(\alpha,\ \beta\)\\)，它们不相交，并集恰好为 \\(A\\)；Dedekind 分割首先是划分，在此之上加入了两个条件，分别是向下封闭，以及无最大元。

$$
    \text{Definition (Dedekind Cut):} \\\\[1ex]
    \text{Dedekind cut is a partition that } A = \mathbb{Q},\ \alpha \cup \beta = \mathbb{Q},\ \ \alpha \cap \beta = \varnothing,\text{ and: }\\\\[0.8ex]
    \begin{aligned}
        &\text{1. } \forall\ x \in \alpha, \ \forall\ y \in \beta\ \Rightarrow\ x < y. \\\\
        &\text{2. } \forall\ x \in \alpha, \ \exists\ y \in \alpha\ \Rightarrow\ x < y.
    \end{aligned}
$$

向下封闭对应上文中的 1，如果一个元素在某集合中，那么所有比它小的数也在这个集合中；无最大元对应上文中的 2，指集合中无最大元素。

在 \\(\mathbb{Q}\\) 上选取符合上述条件的两个子集组成一对，就称为一个 Dedekind 分割，但其实当这一对中的子集确定其中一个，另外一个就确定了。所以可以只使用这对子集中较小的集合来代表这个 Dedekind 分割，称这个集合为下集，即 \\(\alpha\\)。

在所有的 Dedekind 分割中，\\(\beta\\) 可能会出现两种情况，\\(\beta\\) 有最小元，以及 \\(\beta\\) 无最小元。

这里是核心，\\(\beta\\) 有最小元的对应了已明晰的有理数，而 \\(\beta\\) 无最小元的情况则对应了有理数上的空洞。

然而一个重要且容易被误解的地方是，认为 \\(\beta\\) 无最小元的情况对应了新的数，即实数，这个数夹在 \\(\alpha,\ \beta\\) 之间，可以被唯一确定。然而，这是既不能确定，也不能保证唯一的。

这种误区是因为，将在夹缝中的“数”简单的理解为其形式类似自然数或有理数的，可以被明确描述的。然而哪怕假设夹缝中的数是可以被明确描述的，也没有理由认为两个不相交的数集之间只存在唯一的数，因此无论如何，都是错误的。

回到刚刚的想法，那时提到，Dedekind 分割直接通过迫近超越数的过程本身来定义实数。迫近的过程就是 Dedekind 分割的下集，这种向下封闭又无最大元的集合本身可以抽象并定义为实数。

如果 Dedekind 下集作为一个数，那么它是唯一确定的。因为划分本身是唯一的，不存在相同下集的两个不同划分；由于集合本身是无限的，只能通过描述法来构造 Dedekind 下集，是自明而确定的。

$$
    \text{Definition (Real Numbers):} \\\\[1ex]
    \text{A real number is any subset of } \mathbb{Q} \text{, that can form the lower set of a Dedekind cut.} \\\\[0.8ex]
    \mathbb{R} := \\{\ \alpha \subset \mathbb{Q}\ \mid\ \alpha \text{ satisfies following 1 - 3 } \\} \\\\[0.8ex]
    \begin{aligned}
        &\text{1. } \alpha\neq\varnothing,\ \alpha\neq\mathbb{Q} \\\\
        &\text{2. } \forall\ x \in \alpha, \ \forall\ y \in \beta\ \Rightarrow \ x < y. \\\\
        &\text{3. } \forall\ x \in \alpha, \ \exists\ y \in \alpha\ \Rightarrow \ x < y. \\\\
    \end{aligned}
$$

任何一个实数都是一个 \\(\mathbb{Q}\\) 子集的集合，换一种说法，一个实数可以被看作是一个集合，可以在被抽象的实数概念中看到它具体只是作为迫近集合的一个符号是重要的。

## 实数的性质 / 确界存在原理

比较自然的问题是，Dedekind 下集的构造是相当严苛的，迫近的集合从负轴的任意远处都有元素，这样的迫近虽然解决了定义问题，但无法解决更多的问题。

如从在圆内接正六边形开始，不断增加内接正多边形的边数，其构成的迫近集合是否是一个实数？如果在圆内接正多边形时，每次增加的正多边形边数不同，构成了不同的迫近集合，其表示的是否又是同一个实数？

确界存在原理作为 \\(\mathbb{R}\\) 的性质，得到了蕴含在 \\(\mathbb{R}\\) 定义中的结论，同时解决了上述疑问，当然，答案当然是肯定的。

从 Dedekind 分割证明确界存在定理，首先要了解由其定义的实数的序关系是如何定义的。

$$
    \text{Definition (Total Ordering).} \\\\[1ex]
    \text{The total ordering on the real numbers is given by the following expression: } \\\\[0.8ex]
    x\leq y\Leftrightarrow x\subseteq y
$$

在 Dedekind 分割定义的实数系统中，全序关系（即任意两个数的比较）被定义为其各自的集合是否为对方的子集。

这是直观的，如果其中一个下集中出现了对方的上集元素，则根据向下封闭的性质，可以判断集合的迫近超过了对方。

$$
    \text{Principle (Supremum Principle).} \\\\[1ex]
    \text{Every non-empty, bounded-above subset of } S \subset \mathbb{R} \text{, above has a supremum.} \\\\[2.5ex]
    \text{Proof.} \\\\[1ex]
    \text{Let } S \text{ is bounded-above, } \alpha = \textstyle \bigcup_{x \in S} \alpha_x,\ \alpha_x \text{ is a Dedekind Cut lower set of x.} \\\\[0.8ex]
    \text{i. } \alpha \text{ is a upper bound: } \forall x \in S,\ \alpha_x \subset \alpha \Rightarrow x \le \alpha. \\\\[0.8ex]
    \text{ii. } \alpha \text{ is a supremum: } \\\\[0.8ex]
        \quad \text{ if there is another upper bound } \beta, \text{ then } \alpha \subset \beta \\\\[0.8ex]
        \quad \Rightarrow \beta \text{ is minimal at } \alpha. \text{ i.e. } \alpha \text{ is supremum.}
$$

通过利用刚刚提到的实数的全序关系的集合比较方法，可以在证明的过程中使用集合的性质；在证明方法上，一方面，逻辑上非常重视将实数直接作为集合，另一方面，利用简单的反证法应用集合子集推论。

确界存在原理的宏观，是 Dedekind 分割定义的实数推出的一个性质，可以从一个非空有上 / 下界的集合确定一个 Dedekind 分割下集。

其中的巧思是即使目前感兴趣的迫近集合并不是 Dedekind 分割下集，然而其中的元素却可以看成完整的 Dedekind 分割下集，它们的并可以进一步得到原本迫近集合的 Dedekind 分割下集，即确定一个实数。

任何非空有上 / 下界集合都可以确定一个实数（在同时有上下界的情况下是两个，但这与主要思想无关）。

这些内容对于我们**真正**理解数学分析、微积分的所有内容都是有着至关重要的作用的。
