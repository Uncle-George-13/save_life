# Deep Anomaly Detection and Search via Reinforcement Learning



摘要 

半监督学习--通过一小部分有标签的学习特征

对比半监督学习，提出问题，对已有标签的数据挖掘不足，对未标签的数据挖掘不足

提出用强化学习







思想：集成学习思想，分层数据集，（**分层数据集是关键**）

成果：对受污染的未标签的数据集，（测试集中包含未知异常类）

表格试半监督 ： 

解释半监督：训练用一个mini有标签的，和其他没标签的

深度学习中的分布是什么意思？

exploitation and exploration 开发和探索 -- 也可以理解为长期和短期的奖励





 deep learning with Q-learning (deep and RL 的结合)

三类（value ,policy, actor-critic ）



算法介绍：

数据集:

1.一个异常数据集（数据量小）

2.一个没标签的数据集（有正常有异常）

异常得分---------异常 > 正常



组成：

1. SAC-based agent

2. anomaly search environment 

   (1)将数据集分为三部分 （分层数据集）（U（unlabled），T(temporary)，A(anomoly)）

   (2)集成的采样函数 

   (3)奖励函数：supervised and unsupervised rewards.

conf(S(t)) 表示认为是异常的置信度

T Hscore 阈值超参数，和异常评分（action）比较

T Hconf 阈值超参数,和异常置信度比较（conf(S(t))）--- 这里s表示的是数据，用数据充当状态



state：所有训练数据，

Action: 范围[0,1]，是输入数据的异常评分







#### 实验

数据集（5个单独异常，3个多异常数据）



评估指标（AUC-POC曲线，污染率，）