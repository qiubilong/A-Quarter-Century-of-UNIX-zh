# 标准

来自市场的压力和用户的需求驱动着建立一个Unix的标准。在不到10年的时间里市场不断激增。在第10年到来的时候，许多公司诞生了。大多数销声匿迹了，一些幸存下来。不兼容的软件和硬件大量出现是日益增长的厂商们主要的问题。不像1956年到1978年这段时间，当时几乎每一个计算机中心都处在单一的阴影中——通常是蓝色。微型计算机和工作站——苹果，PC，微软——都在改变这些。

这里分为两种:系统标准和语言标准。其中第二种(C语言标准)是完善的:美国国家标准协会成立了X3J11委员会——C编程语言——试图定义ANSI标准X3.159-1989，之后成为国际标准，ISO/IEC 9899:1990。

操作系统标准的建立经历了曲折的过程。Unix标准起始于Heinz Lycklama向/usr/group董事会提议建立了一个标准委员会。1984年在委员会的努力下制定了一份/usr/group标准并被成员接受。虽然它没有官方身份，/usr/group还是非常有影响力的:当ANSI X3J11成立的时候，它使用这份标准作为C语言库部分的基础。总之，随着System 4，4.xBSD，和XENIX的开发分支不断出现，/usr/group标准很快就不再适用。

在1985年早期，/usr/group委员会与新成立的IEEE POSIX(电子和电子工程协会，可移植操作系统)工作组合并，/usr/group标准被接受成为第一版草稿。

到1989年POSIX分化出了10个子委员会。4年以后，子委员会数量超过20个，虽然只有两个标准——不可否认是最重要的——被修订(POSIX.1和POSIX.2)。还有一个POSIX.0文档:POSIX开放系统环境简介，试图解释应用程序的移植。

无论如何，意识到POSIX不是Unix是很重要的。它是一个借口，不是一个实现。Fred Zlotnick曾经将POSIX称为“Unix的一个归纳”。POSIX.1提出了很多Unix的概念并将它们替换为一种抽象，这样将大量其他方面不兼容的系统可以称之为“遵从POSIX的”。因为标准越来越被市场所驱动，相比于技术驱动，它很难预料它的结果。行业工会发布的大量标准对于用户并没有什么帮助。

例如，1985年1月，AT&T发布了它的《System V接口规范》(SVID)，一个“有版权，无专利的开放系统文档”。一个新版本在5年后发布。在这期间，X/Open发布了它的《移植指南》(XPG)，现在它已经有了几个版本:XPG2，XPG3，XPG4。XPG3和XPG4在某些方面超越了SVID。

88open是一个“公司和个人致力于基于摩托罗拉88000 RISC处理器家族创建一个多厂商，开放计算环境”的团体。它建立与1988年。这个联营企业发布了一个资料读物和一个“开放系统参考指南”:《标准世界》。我将在后面的章节再详细介绍开放软件基金会和Unix国际化。

Unix会议的20周年纪念会议上，Ritchie评论C语言标准和POSIX:

> 我们为Unix标准化做了相当小的贡献。最大的合作是为POSIX shell做了一些改良。

> 和C语言标准相似，我谨慎的避开了X3J11。当Larry Rosler和Dave Prosser是草稿校订者并且AT&T身处委员会时，我和他们做了一些幕后的合作。但随着著名的无记名例外，我太多嘴，没有参与进去...

> 我觉得C语言标准是个很棒的工作。实际它几乎是一个成功的标准化成果的模型。他们将一些本质上没问题但是实际上需要净化和更新的东西在不破坏的前提下净化更新了。当然可以有很多批评...但是，当你对比其他语言的情况，像FROTRAN 8X甚至是Pascal，当有一个标准来规范，C语言的命运更加让人高兴。

Ritchie对于POSIX的成果没有很大的兴趣:

> 这是一个混合的袋子。系统调用和程序库甚至是命令看起来相当合理，争议和搞砸都还不坏。着这个结果上产业界看起来很不错。换句话说，这部分缺乏一些很显而易见的东西，就像网络的连贯一致。Presotto和我几年前谈论USENIX的一种方法...无论如何，我们的方法看起并没有接管世界。

> 同样，IEEE POSIX的成果看起来是一种糟糕的方式，它吓到了大多数的人们。特别是，实时组看起来聚集了所有未被充分理解的点子，他们看上去和已有的系统不想匹配。我现在担心程序任务的想法，几个小的进程在同一个内存镜像里执行，因为Unix和它的软件并不能很好的适应——C语言不支持，程序库也不支持。多处理器在你设计软件时有很多暗示，我害怕仅仅列出来会导致混乱。

> 说我自我矛盾是保守的!标准化产生的不安在很多方面是非常巨大的。

> 经常提到的一个是创新和标准化的矛盾，我觉得这不是一个真正的问题。如果有了标准，你可以精心的选择是遵从它们还是做些其他的。这是一场赌博，但是是最合理的一个。真正的问题是还没有决定特定范围是否应该标准化。当一个应该制定的唯一标准(VHS和XBeta)还没有做出来才是真正可怕的。

> 人们应该意识到的是和我们相关的许多标准是由非常小的小组制定的，如果你足够关心并且以正确的方式工作，他们会受到影响。在起草阶段，一个恰当的主张，一个具体的建议都大有帮助。这是悖论的一部分，当然，它意味着一些很棒的人可以挽救大局，但是也意味着一些愚蠢的人可以把事情搞砸好几年。

自从Ritchie的评论发表后，POSIX子委员会的数量渐渐变多，他们之中只有少部分有提议并继续投票。后来，随着更多工会的成立，非正式标准的数量随着几个IEEE委员会所做的事情一起变多。
