# 强化学习简介

强化学习（Reinforcement Learning，RL）被视为与监督学习和无监督学习并列的基本机器学习范式之一。RL 关注的是决策：做出正确的决策，或者至少从中学习。

想象一下你有一个模拟环境，比如股票市场。如果你实施了一项规定，会发生什么？它会产生积极还是消极的影响？如果发生了消极的事情，你需要从这个_负强化_中学习并改变方向。如果是积极的结果，你需要在这个_正强化_的基础上进一步发展。

![彼得和狼](../../../translated_images/peter.779730f9ba3a8a8d9290600dcf55f2e491c0640c785af7ac0d64f583c49b8864.zh.png)

> 彼得和他的朋友们需要逃离饥饿的狼！图片由 [Jen Looper](https://twitter.com/jenlooper) 提供

## 地区主题：彼得与狼（俄罗斯）

[彼得与狼](https://en.wikipedia.org/wiki/Peter_and_the_Wolf) 是由俄罗斯作曲家 [Sergei Prokofiev](https://en.wikipedia.org/wiki/Sergei_Prokofiev) 写的一部音乐童话。故事讲述了年轻的先锋彼得，他勇敢地走出家门，来到森林空地去追逐狼。在本节中，我们将训练机器学习算法来帮助彼得：

- **探索** 周围区域并建立最佳导航地图
- **学习** 如何使用滑板并在上面保持平衡，以便更快地移动。

[![彼得与狼](https://img.youtube.com/vi/Fmi5zHg4QSM/0.jpg)](https://www.youtube.com/watch?v=Fmi5zHg4QSM)

> 🎥 点击上面的图片听 Prokofiev 的《彼得与狼》

## 强化学习

在前面的章节中，你已经看到了两种机器学习问题的例子：

- **监督学习**，我们有数据集来建议我们想要解决的问题的样本解决方案。[分类](../4-Classification/README.md) 和 [回归](../2-Regression/README.md) 是监督学习任务。
- **无监督学习**，我们没有标记的训练数据。无监督学习的主要例子是 [聚类](../5-Clustering/README.md)。

在本节中，我们将向你介绍一种不需要标记训练数据的新型学习问题。有几种类型的此类问题：

- **[半监督学习](https://wikipedia.org/wiki/Semi-supervised_learning)**，我们有大量未标记的数据，可以用来预训练模型。
- **[强化学习](https://wikipedia.org/wiki/Reinforcement_learning)**，其中一个代理通过在某些模拟环境中进行实验来学习如何行为。

### 示例 - 电脑游戏

假设你想教电脑玩游戏，比如国际象棋或 [超级马里奥](https://wikipedia.org/wiki/Super_Mario)。为了让电脑玩游戏，我们需要它预测在每个游戏状态下应该做出哪一步。这看起来像是一个分类问题，但实际上不是——因为我们没有一个包含状态和相应动作的数据集。虽然我们可能有一些现有的象棋比赛或玩家玩超级马里奥的记录数据，但这些数据可能不足以涵盖足够多的可能状态。

与其寻找现有的游戏数据，**强化学习**（RL）基于*让电脑多次玩游戏*并观察结果的想法。因此，要应用强化学习，我们需要两样东西：

- **一个环境**和**一个模拟器**，允许我们多次玩游戏。这个模拟器将定义所有的游戏规则以及可能的状态和动作。

- **一个奖励函数**，告诉我们每一步或每局游戏的表现如何。

其他类型的机器学习与 RL 的主要区别在于，RL 中我们通常不知道是否赢得比赛，直到比赛结束。因此，我们无法判断某个单独的动作是否好——我们只在游戏结束时获得奖励。我们的目标是设计能够在不确定条件下训练模型的算法。我们将学习一种称为 **Q-learning** 的 RL 算法。

## 课程

1. [强化学习和 Q-Learning 简介](1-QLearning/README.md)
2. [使用健身模拟环境](2-Gym/README.md)

## 致谢

"强化学习简介" 由 [Dmitry Soshnikov](http://soshnikov.com) 倾情撰写

**免责声明**：
本文件是使用基于机器的人工智能翻译服务翻译的。尽管我们努力确保准确性，但请注意，自动翻译可能包含错误或不准确之处。应将原始语言的文件视为权威来源。对于关键信息，建议使用专业的人类翻译。对于因使用本翻译而引起的任何误解或误读，我们不承担责任。