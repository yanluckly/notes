## 合适编写生成器

本质上讲，使用生成器有两个主要的理由。这两个理由来自于相同的基本概念：只有当需要值时才会确定这个值，而不是提前准备好。

这里的基本原则就是：通过自己的代码提前去做一系列工作活存储一堆数据是没有好处的。通常并不需要大的数据块。即使需要所有数据，但是入宫不需要一次性处理所有数据，任然可以仅存储需要的数据。

从基本原则中扩展出来的两个出例都需要分块分文数据，还需要分块计算数据。

### 分块访问数据

编写生成器的首要原因是需要涵盖需要分块访问数据的情况，但是这种情况下没必要存储整个副本。

这正是之前介绍的文件对象生成器与dict.items方法中本质上所发生的事情。处理小文件时，将整个温江读到内存是非常合适的，并且可以对内存中字符串做任何需要的处理。

另一方面，如果文件很大。如果需要重建一个大型的字典呢？有时，将操作数据复制到内存中并不是可行的操作。这是，就需要分块访问数据。

### 分块计算数据

编写生成器的第二个常见理由是仅在需要它时计算数据。考虑一下本章前面讨论range函数和fibonacci函数。必须驯悍遍历0到最导致之前每个数字的程序不必存储包括范围内每个数字的列表。对于每次支队当前数字家1知道达到最大值而言，内存是足够的。

与之相似，fibonacci函数不需要计算每个斐波那契数字。生成器仅仅需要确定下一个单一的斐波那契数列并且输出它。

因为有时序列中的每个元素的计算可能相当昂贵，所以这可能是很重要的理由，而且计算整个系列的数据是没有价值且没有必要的。
