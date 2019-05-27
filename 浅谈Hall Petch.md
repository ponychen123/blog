# 浅谈Hall Petch关系(一)

我想做结构材料的没有人不清楚Hall Petch关系，它反映了材料强度与晶粒的尺寸的开方成反比。极小晶粒下的反 Hall Petch 关系也一度成为热点。不过本文并不关注实验现象，下面的文章我只是按照个人见解简要介绍一些经典的 Hall Petch 理论。从Hall Petch 关系提出至今，研究人员为了解释这个现象提出了大量的理论，我从中提取了几个典型的理论做简要介绍。1951年，Hall[^1] 发表的论文中除了报导Hall Petch关系，也首次提出了pile up(位错阻塞)模型。

![1558524271798](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\1558524271798.png)

简单起见，我们不妨假设左边晶粒的中心O点存在一个位错源，在外加应力的作用下位错源沿着某一滑移面释放出一系列位错。随着第一个发射的位错冲撞到晶界AB上，整个位错列队被禁锢在位错源与晶界之间。由于晶界的阻力和新产生位错的弹性应变，整个位错列最后会形成一个稳定分布，假设晶粒的平均尺寸为d，则位错列中位错的数目为(不知道这公式怎么来的请自裁)：

![1558524939284](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\1558524939284.png)

其中$\tau$e表示位错的有效剪切应力，它可以表示为

![1558525016677](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\1558525016677.png)

显然，它实际上是在加载应力中扣除了弹性应力部分。试想如果你要产生一根位错，首先晶体要发生塑性变形，因此塑性变形前的弹性部分并不是我们应该要考虑的部分。既然我们已经知道位错列中位错的数目，如果我们粗略地认为，所有的位错作用到晶界上的应力都是等效的，那么晶界上受到的应力$\tau$p为

![1558526098315](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\1558526098315.png)

Hall认为，材料屈服发生于位错列冲破晶界的时候，也就是说$\tau$p大于临界值$\tau$c。如果我们取等号，再将前面的n代入，我们就可以得到

​                                                                  ![1558526526580](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\1558526526580.png)

嗯。。看着很合理，-1/2次方也出来了。但是我们细想一下，如果材料的屈服依靠的是位错像裂纹一般冲破晶界，我们应该在实验中大量发现，但实际上，至少从笔者的角度，笔者只看到过少数几篇文献报导过。更重要的是，依据该理论计算的屈服强度跟实际数据还是有点出入的。

在pile up模型的基础上，Cotrell[^2]认为，材料的屈服并非来自于位错列冲破晶界，而是由于位错列在晶界的终端的应力场诱发了邻近晶粒中的位错源(如下图的R处)的开动。这样子需要的 临界应力要小于pile-up模型。

![1558527114621](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\1558527114621.png)

晶粒内部出现位错源固然可行，但是晶界本身就是天生的位错源，那为什么我们不认为位错起源于晶界呢？当然有研究者早就付诸于实践。Li[^3]于1963年就提出了boundary source模型。为了方便起见，我们不妨假设晶粒是边长为d的立方体。假设晶粒的每一个面上的台阶密度为m，假设每一个台阶都有一定几率发射位错。进一步简化，我们干脆认为每个台阶都会发射位错，则一个面的总位错数目为$md^2$。每一个晶粒与毗邻晶粒公用一个晶面，则一个晶粒可以认为有三个晶界面属于这个晶粒。所以

![1558602619480](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\1558602619480.png)

我们干脆认为一个晶粒有3$md^2$个位错。这些位错在外加应力作用下继续向晶内扩散，形成位错林。位错林的密度为

![1558610496216](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\1558610496216.png)

我们很容易联想到，晶体材料的位错密度和强度可以由著名的Taylor公式来描述

![1558610702112](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\1558610702112.png)

代入前者即得

![1558610795599](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\1558610795599.png)

我们又获得了Hall Petch关系。在原文中也说明这个方式计算的理论屈服强度与pile up模型基本一致。重新审视这两个模型，前者认为位错完全起源于晶粒内部，后者则认为位错完全起源于晶界，两者分别是实际情况的两个极端。但是殊途同归，两个极端最后得到了相同的结论和近似的屈服强度。当然我们可以抨击这两个模型都不符合实际，但比起实际，这种抽象于现实的理论模型，我认为更加具有美学的科学特征。不过，这两个模型的局限性也是明显的，实验中Hall Petch曲线的斜率对晶粒结构和化学成分非常敏感，但是上述模型的前提就扼杀了描述这种现象的可能性。

在02年的一篇文章[^4]中，该文作者也成功在MD模拟中发现的晶界出位错的形核和发射过程。

![1558611333978](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\1558611333978.png)

好了，这个部分先到此结束，如果还有机会的话，我会继续介绍下一阶段的Hall Petch模型。

**PS：本文章推导只是作者本人根据文章以自己的理解推导的，想要了解真正严格推导的请自己查看原文。本人概不负责。**

ponychen  20190523

email:18709821294@outlook.com

 [^1] Hall, E. O. "The deformation and ageing of mild steel: III discussion of results." *Proceedings of the Physical Society. Section B* 64.9 (1951): 747.

 [^2] A.H. Cottrell,: The Mechanical Properties of Matter, Wiley, New York (1964) 

 [^3]Li, James CM. "Petch relation and grain boundary sources." *Transactions of the Metallurgical Society of AIME* 227.1 (1963): 239.

 [^4]Van Swygenhoven, H., P. M. Derlet, and A. Hasnaoui. "Atomic mechanism for dislocation emission from nanosized grain boundaries." *Physical Review B* 66.2 (2002): 024101.