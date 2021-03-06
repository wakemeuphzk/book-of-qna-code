# 隐马尔可夫模型

一阶隐马尔可夫模型，以及维特比算法、前后向算法和Baum-Welch算法的实现。

如果使用本书附带的[docker镜像](https://hub.docker.com/r/chatopera/qna-book/)，所有依赖已经安装好，不需要再次安装。使用docker镜像运行程序的方式详见[文档](https://github.com/l11x0m7/book-of-qna-code/blob/master/README.md)。

## UML

模块之间的关系

<img src="./packages.png" width="200">

核心类的接口和类之间的关系

<img src="./classes.png" width="400">

## 前向算法

* 预测：计算给定观测序列的发生概率

```
python test.py Test.testObservationProbForward
```

## 后向算法

* 预测：计算给定观测序列的发生概率

```
python test.py Test.testObservationProbBackward
```

前向算法与后向算法对同一个观测序列的预测概率是一致的，二者只是计算起点不同。二者的时间复杂度也是一致的。

## 维特比算法

* 解码：对于给定的观测序列，寻找最优的状态序列

```
python test.py Test.testViterbi
```

## Baum Welch算法

* 模型参数估计：在给定可观测序列的基础上，使用EM算法学习HMM的参数

```
python test.py Test.testBaumWelchTrain
```