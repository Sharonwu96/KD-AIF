# Knowledge Distillation with Adaptive Influence Weight (KD-AIW)

This repository provides **example code** for the method proposed in the following paper:

**“[Knowledge distillation with adapted weight](https://arxiv.org/pdf/2501.02705)”**  
**Wu S, Luo X, Liu J, Deng Y.**  
*Statistics*, 2025, 59(2): 470–497.  


## Description

This repository demonstrates a practical implementation of the **KD-AIW** framework proposed in the paper. The method dynamically adjusts the weights of training samples during the knowledge distillation process, based on their estimated influence on a validation set.

### Influence Function Reference

Influence score computation in this repository is based on the original method proposed in the ICML 2017 best paper:  
**[Understanding Black-box Predictions via Influence Functions](https://arxiv.org/abs/1703.04730)**  by *Pang Wei Koh* and *Percy Liang*.

We use a PyTorch reimplementation, and partially refer to the [code](https://github.com/kohpangwei/influence-release).

While **[Kronfluence](https://github.com/pomonam/kronfluence)** supports more efficient influence computations for large-scale models using **EK-FAC** (Empirical Kronecker-Factored Approximate Curvature), our code also provides a minimal working implementation tailored to small-to-medium image classification models like ResNet on CIFAR datasets.
