# CAMEL: Communicative Agents for “Mind” Exploration of Large Scale Language Model Society.

## 所解决的问题？

目前的语言模型还是需要人类的输入来进行指导对话，在时间开销上会很大。这篇文章提出一种新的智能体通信框架角色扮演(role-playing)。作者采用了一个叫做初始Prompt的东西(inception prompting)来做这样一件事情。也就是只在开始人为给定prompt，之后就全靠智能体自己去对话探索了。


人话来说就是，目前主流的基于大模型的应用都是人肉去调prompt，这个非常耗费开销。作者提出了一种方法，让智能体之间进行对话，进而自动去完成任务，而过程中无需人为干预。

## 背景

目前多智能体间的通信也是研究的一个热点问题，但是主流的通信是基于一些只有智能体才能看懂的向量。而人类语言间的通信能否作用到计算机里面呢？实现智能体间的通信？或者更近一步实现人机通信，人机协作？

知识蒸馏可以实现知识从老师到学生之间的传递，大体也是可以被分成三类：Response-based, Feature-based, and Relation-based。更多的是去抓住模型中的知识，而作者所提出来的方法，是去处理对话智能体“思想”上的探索。

## 所采用的方法？

大体上是有两个智能体，也就是大语言模型：AI assistant和AI user。当给定一个初始的任务时，一个task-specifier agent将会将任务拆解，描绘更加细致的任务给到AI assistant和AI user，然后他两就开始对话完成任务了：

![](https://img-blog.csdnimg.cn/93be71118001406aab2dd96ac5786cb2.png#pic_center)

另外作者还提及到了一些在设计prompt的时候需要注意的点：

1. 在两个智能体对话的时候，常常会角色互换，因此需要好好设计一下这个prompt，比如对于AI assistant，就告诉他，好好执行就行了，不要提问题。
2. 另一个是assistan repeats，assistant会重复user‘s 的prompt。
3. 虚假回复，比如assistant保证会完成某个任务，实际上没有完成。
4. 无限消息循环，智能体之间的消息无限循环。

## 取得的效果？

作者也就是对这个实验结果做了一些分析，可视化等等就完事了。
## 问题

## 所出版信息？作者信息？

- King Abdullah University of Science and Technology (KAUST)

## 参考链接

- 开源地址：https://github.com/lightaime/camel