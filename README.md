P-EPC: Pre-trained Evolutionary Parameter Controller

Introduction / 简介

(1) P-EPC is an open-source framework designed for learning-assisted evolutionary parameter control.
(2) Unlike traditional in-situ reinforcement learning (RL) methods that learn from scratch for every new task, P-EPC decouples policy learning from the optimization process.
(3) By interacting with a distribution of problem classes during an offline pre-training phase, the agent extracts shared evolutionary dynamics and provides real-time adaptive parameters via direct inference on new instances.

(1) P-EPC 是一个开源的强化学习辅助进化参数控制框架 。
(2) 不同于传统的需要在每个新任务中从零开始学习的在位学习（in-situ learning）方法，P-EPC 将策略学习与优化过程进行了时间上的解耦 。
(3) 通过在离线预训练阶段与特定问题类的分布进行交互，代理（Agent）能够提取共享的进化动力学特征，并通过直接推理为新实例提供实时的自适应参数 。

Core Features / 核心特性

(1) Decoupled Learning Paradigm / 解耦学习范式
Temporally separates policy training from the search process to eliminate repetitive gradient updates and computational overhead during optimization.
在时间上将策略训练与搜索过程分离，消除了优化过程中重复的梯度更新和计算开销 。

(2) Scale-Invariant State Representation / 尺度不变的状态表示
Utilizes population statistical features (e.g., dispersion, fitness gaps, and evolution rates) to ensure robust perception across varying problem scales and dimensions.
利用种群统计特征（如离散度、适应度间隙和进化速率）来确保在不同问题规模和维度下的稳健感知 。

(3) Dual-Track Relative Time Reward / 双轨相对时间奖励
Maps absolute fitness values into a unified, dimensionless time metric space to achieve value alignment across heterogeneous tasks and reduce gradient variance.
将绝对适应度值映射到统一的无量纲时间度量空间中，从而实现异构任务之间的价值对齐并降低梯度方差 。

(4) High-Throughput Computing Platform / 高吞吐计算平台
Features a dual-engine architecture with Just-In-Time (JIT) compilation and zero-copy shared memory to significantly accelerate environmental interactions.
采用具备即时编译（JIT）和零拷贝共享内存的双引擎架构，显著加快了环境交互速度 。

(5) Scalable Benchmark Suite / 可扩展的基准测试集
Includes 20 parameterized physical and engineering problem classes (P1–P20) with support for domain randomization to test policy generalization.
包含 20 个参数化的物理和工程问题类（P1–P20），支持领域随机化以测试策略的泛化性能 。

(6) Strict Data Isolation / 严格的数据隔离
Implements an instance-level isolation protocol (Training/Validation/Test) to verify that the controller learns generalizable search rules rather than memorizing specific landscapes 。
实施实例级隔离协议（训练/验证/测试），以验证控制器学习到的是可泛化的搜索规则而非对特定地形的记忆 。
