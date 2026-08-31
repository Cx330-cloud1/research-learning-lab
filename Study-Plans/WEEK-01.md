# 第一周｜科研基础启动

## 本周目标

第一周的重点不是"刷完课程"，而是建立一套可以长期使用的科研学习工作流。

本周结束时，应尽量做到：

-   能独立编写一个简单的科研数据处理 Python 脚本；
-   理解 PyTorch 中 Tensor、Dataset、DataLoader、Model 和基础训练循环；
-   能解释向量、线性组合、矩阵乘法与 `Ax = b` 的基本含义；
-   使用固定模板完成至少 3 篇论文的结构化阅读；
-   初步建立共情对话 / 情感支持对话研究版图；
-   提出至少 5 个值得继续追踪的研究问题。

## 本周核心产出

-   `dialogue_statistics.py`
-   `tensor_basics.py`
-   `dialogue_dataset.py`
-   `emotion_classifier.py`
-   `training_loop.py`
-   线性代数学习笔记
-   至少 3 篇结构化论文笔记
-   Empathetic / Emotional Support Dialogue Landscape V1
-   至少 5 个初始 Research Questions
-   Week 1 Summary

------------------------------------------------------------------------

## Day 1｜Python 科研基础 + 线性代数 + 论文阅读

### Python for Research｜2h

学习：

-   变量与基本数据类型
-   list / tuple / dict / set
-   `if` / `for` / `while`
-   函数
-   文件读写
-   `pathlib`
-   JSON
-   CSV
-   异常处理

练习：

建立一个简单的对话数据集，实现：

-   `load_data()`
-   `count_emotions()`
-   `count_strategies()`
-   `save_statistics()`

输出：

`02-Programming/Python/exercises/dialogue_statistics.py`

### Linear Algebra｜1.5h

课程：

[MIT 18.06 --- Linear
Algebra](https://ocw.mit.edu/courses/18-06sc-linear-algebra-fall-2011/)

重点理解：

-   Vector
-   Linear Combination
-   System of Linear Equations
-   `Ax = b` 的列视角
-   Matrix Multiplication 的直觉

笔记中回答：

1.  什么是向量？
2.  什么是线性组合？
3.  如何从列向量角度理解 `Ax = b`？
4.  为什么矩阵乘法有意义？
5.  在机器学习中，`X` 和 `W` 可以分别代表什么？

输出：

`01-Mathematics/Linear-Algebra/README.md`

### Paper Reading｜1.5h

论文：

[Rashkin et al., 2019 --- Towards Empathetic Open-domain Conversation
Models](https://aclanthology.org/P19-1534/)

按照以下结构阅读：

-   Research Question
-   Motivation
-   Previous Limitation
-   Dataset
-   Task
-   Method
-   Metrics
-   Results
-   Limitations
-   My Questions

重点思考：

-   为什么需要单独建立 empathy benchmark？
-   EmpatheticDialogues 实际测量的是 empathy 的哪一部分？
-   哪些假设放到今天的 LLM 环境中可能已经过时？

输出：

`08-Research-Skills/Paper-Reading/notes/2019-empathetic-dialogues.md`

### Research Log｜1h

记录：

-   今天真正理解了什么？
-   最大的困惑是什么？
-   今天的数学 / 编程知识与科研有什么联系？

------------------------------------------------------------------------

## Day 2｜NumPy + PyTorch Tensor

### NumPy｜1.5h

学习：

-   array
-   shape
-   reshape
-   axis
-   mean / sum
-   argmax
-   matrix multiplication

练习：

创建矩阵 `X` 和 `W`，计算：

`Y = X @ W`

并解释 `X`、`W`、`Y` 的 shape。

### PyTorch｜2h

课程：

[PyTorch --- Learn the
Basics](https://docs.pytorch.org/tutorials/beginner/basics/)

学习 Quickstart 和 Tensors。

重点：

-   `torch.tensor`
-   `shape`
-   `dtype`
-   `device`
-   `zeros`
-   `ones`
-   `rand`
-   indexing
-   matrix multiplication

输出：

`02-Programming/PyTorch/exercises/tensor_basics.py`

### Linear Algebra｜1.5h

将矩阵乘法与 NumPy / PyTorch 中的 Tensor 运算联系起来。

目标不是继续追求大量新知识，而是理解：

> 数学中的矩阵运算是如何真正进入模型代码的？

### Paper Reading｜1h

完成并整理 EmpatheticDialogues 论文笔记。

------------------------------------------------------------------------

## Day 3｜Dataset / DataLoader + ESConv

### PyTorch｜2.5h

课程：

[Datasets &
DataLoaders](https://docs.pytorch.org/tutorials/beginner/basics/data_tutorial.html)

学习：

-   `Dataset`
-   `DataLoader`
-   batching
-   shuffling
-   iteration

练习：

实现一个简单的 `DialogueDataset`，包含：

-   dialogue text
-   emotion label

输出：

`02-Programming/PyTorch/exercises/dialogue_dataset.py`

### Linear Algebra｜1.5h

学习：

-   Elimination
-   Matrix Operations
-   Invertibility 的基本直觉

只完成少量代表性练习，不追求刷题数量。

### Paper Reading｜1.5h

阅读 ESConv / Emotional Support Conversation 相关论文。

重点回答：

> EmpatheticDialogues 中的"共情"和 ESConv 中的"情感支持"究竟有什么区别？

完成第二篇结构化论文笔记。

------------------------------------------------------------------------

## Day 4｜神经网络基础 + 实验表格阅读

### PyTorch｜2h

课程：

[Build the Neural
Network](https://docs.pytorch.org/tutorials/beginner/basics/buildmodel_tutorial.html)

学习：

-   `nn.Module`
-   `__init__`
-   `forward`
-   `nn.Linear`
-   Activation Functions
-   `nn.Sequential`

练习：

实现一个最小版本的 `EmotionClassifier`。

要求：

能够解释每一层输入和输出 Tensor 的 shape。

输出：

`02-Programming/PyTorch/exercises/emotion_classifier.py`

### Linear Algebra｜1.5h

用神经网络中的：

`Y = XW + b`

重新理解矩阵乘法。

目标是能够解释：

-   `X` 是什么；
-   `W` 是什么；
-   为什么维度必须匹配；
-   输出维度如何确定。

### Research Skills｜1.5h

选择一张论文实验结果表进行阅读。

回答：

-   每一行代表什么？
-   每一列代表什么？
-   使用了哪些指标？
-   方法究竟提升了多少？
-   实验结果是否足以支持作者的 claim？
-   是否报告统计显著性或不确定性？

输出：

`08-Research-Skills/Paper-Reading/paper-reading-checklist.md`

### Paper Reading｜1h

完成或修改 ESConv 论文笔记。

------------------------------------------------------------------------

## Day 5｜Research-only Day

今天不以"看课程"为主要任务。

### Research Landscape｜3h

建立：

**Empathetic / Emotional Support Dialogue Landscape V1**

初始结构可以是：

``` text
Empathetic Dialogue
|
|-- Emotion Understanding
|-- Response Generation
|-- Emotional Support
|   |-- Support Strategies
|   `-- User State
|-- Emotion Dynamics
|-- Multi-Agent
|-- Personalization
|-- Memory
`-- Evaluation
```

将目前接触到的代表性工作放入研究版图，例如：

-   EmpatheticDialogues
-   ESConv
-   MultiAgentESC
-   EmoDynamiX

这一阶段不要求分类完全正确。

真正重要的是开始建立：

> "这个领域有哪些问题？这些论文分别解决了什么？"的整体认识。

### Research Questions｜1.5h

提出至少 5 个问题。

例如：

-   Support Strategy 是否应该根据用户历史动态变化？
-   单一 emotion label 是否足以表示用户状态？
-   Multi-Agent 方法的提升究竟来自 agent specialization，还是更多
    inference compute？
-   Emotional Support Quality 应该如何超越 lexical similarity 进行评价？
-   长期共情对话真正需要保存什么类型的 memory？

暂时不要求这些问题能够直接成为论文题目。

### Paper Reading｜1h

选择一篇与研究版图中某个分支高度相关的论文阅读。

### Research Log｜0.5h

记录：

> 本周目前发现的最有意思、但尚未解决的问题是什么？

------------------------------------------------------------------------

## Day 6｜完整 PyTorch Training Loop

### PyTorch｜2h

实现一个完整的基础训练循环：

``` python
for epoch in range(num_epochs):
    model.train()

    for x, y in dataloader:
        optimizer.zero_grad()
        output = model(x)
        loss = criterion(output, y)
        loss.backward()
        optimizer.step()
```

加入 evaluation：

``` python
model.eval()

with torch.no_grad():
    ...
```

要求能够解释：

-   `zero_grad()`
-   forward pass
-   loss
-   backward pass
-   optimizer step

输出：

`02-Programming/PyTorch/exercises/training_loop.py`

### Linear Algebra｜1.5h

复习：

-   Vector
-   Linear Combination
-   Matrix
-   Matrix Multiplication
-   `Ax = b`
-   Rank 的基本直觉

能够解释：

-   `X ∈ R^(32×768)`
-   `W ∈ R^(768×256)`
-   `Y = XW ∈ R^(32×256)`

重点理解每一个数字可能对应什么实际含义。

### Python｜1h

回头修改 Day 1 的脚本。

检查：

-   函数是否清晰？
-   命名是否合理？
-   是否存在重复代码？
-   输入异常时是否容易报错？

### Paper Reading｜1h

完成第三篇结构化论文笔记。

### Summary｜0.5h

写下：

> 本周目前最重要的一个技术理解是什么？

------------------------------------------------------------------------

## Day 7｜周复盘 + GitHub 整理

### Weekly Review｜1h

回答：

-   这一周我真正学会了什么？
-   哪些内容已经可以不复制教程独立实现？
-   哪个概念仍然不清楚？
-   哪篇论文最改变我对研究方向的理解？
-   目前哪个 Research Question 最值得继续追踪？

### Repository Cleanup｜2h

整理 GitHub 仓库。

建议结构：

``` text
01-Mathematics/
`-- Linear-Algebra/

02-Programming/
|-- Python/
|   `-- exercises/
`-- PyTorch/
    `-- exercises/

08-Research-Skills/
`-- Paper-Reading/
    |-- paper-reading-checklist.md
    `-- notes/
```

检查：

-   文件名是否清楚；
-   README 是否能解释学了什么；
-   代码是否可以运行；
-   是否留下大量无意义临时文件；
-   笔记是否是自己的理解，而不是复制课程原文。

### Math Review｜1h

先不看笔记，尝试自己解释本周线性代数知识。

解释不出来的地方再返回课程。

### Paper Review｜1h

横向比较本周阅读的至少 3 篇论文。

重点比较：

-   Research Question
-   Dataset
-   Task
-   Method
-   Evaluation
-   Limitation

### Catch-up｜1h

只用于补本周没有完成的高价值任务。

不要为了"完成计划"临时增加低价值工作。

------------------------------------------------------------------------

## 本周验收标准

完成以下 8 项中的至少 6 项，即认为 Week 1 达标：

-   [ ] 完成一个 Python 科研数据处理脚本
-   [ ] 实现 PyTorch Dataset / DataLoader
-   [ ] 实现一个基础 PyTorch Model
-   [ ] 实现完整基础 Training Loop
-   [ ] 完成线性代数笔记，并能够解释 Matrix Multiplication
-   [ ] 完成至少 3 篇结构化论文笔记
-   [ ] 完成 Research Landscape V1，并提出至少 5 个 Research Questions
-   [ ] 完成 Week 1 Summary 并提交 GitHub

## Week 1 Summary 模板

``` markdown
# Week 1 Summary

## 本周学到了什么

### Python

### PyTorch

### Linear Algebra

### Research

## 本周实现了什么

## 阅读论文

## 最重要的一个认识

## 最大的困惑

## 新产生的 Research Questions

## 下周需要继续解决的问题
```

## 本周原则

本周建议投入约 **30--36 小时有效学习时间**。

不以观看课程时长作为完成标准，而以是否留下可以检查的学习与科研产出作为标准。

第一周暂时不要扩展到 LangGraph、RAG、LoRA、Agent Framework、CS336、CUDA
或 Docker。先把 Python、PyTorch、线性代数和论文阅读工作流建立起来。
