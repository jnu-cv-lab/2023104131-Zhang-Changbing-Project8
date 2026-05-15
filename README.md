# PyTorch 图像分类实验 (MNIST)

## 项目简介

本项目使用 PyTorch 实现手写数字识别（MNIST 数据集），完整体验了深度学习图像分类的基本流程：数据加载、模型定义、训练、验证、测试以及结果分析。模型采用改进的卷积神经网络（包含三个卷积层、批归一化、Dropout），并在测试集上达到了 **99.17%** 的准确率。此外，还对比了 SGD 和 Adam 优化器的性能差异。

## 环境要求

- Python 3.8+
- PyTorch 2.0+
- torchvision
- matplotlib
- numpy
- scikit-learn
- seaborn

安装依赖：

```bash
pip install torch torchvision matplotlib numpy scikit-learn seaborn
```

## 文件结构

```
.
├── pytorch_classification.py   # 主程序代码
├── README.md                   # 本文件
├── Report8.doc                 # 实验报告
└── 输出图像（自动生成）:
    ├── sample_images.png       # 训练样本示例
    ├── training_curves.png     # 训练/验证 loss 和 accuracy 曲线
    ├── test_predictions.png    # 测试图像预测结果
    └── confusion_matrix.png    # 混淆矩阵
```

## 运行方法

1. 将代码保存为 `pytorch_classification.py`。
2. 在终端中执行：
   ```bash
   python pytorch_classification.py
   ```
3. 程序将自动下载 MNIST 数据集（首次运行），依次进行训练、验证、测试，并显示：
   - 训练/验证每个 epoch 的 loss 和 accuracy（控制台输出）
   - 样本图像窗口
   - 训练曲线图
   - 测试预测结果图
   - 混淆矩阵图
4. 所有图像会自动保存在当前目录。

## 主要功能

- **任务1：环境准备** – 检查 PyTorch 版本和 GPU 可用性。
- **任务2：加载数据集** – 下载 MNIST，划分训练/验证/测试集，显示样本图像。
- **任务3：定义 CNN 模型** – 改进的 CNN（3个卷积层 + BN + Dropout）。
- **任务4 & 5：训练与验证** – 训练 10 个 epoch，记录损失和准确率。
- **任务6：测试模型** – 在测试集上评估最终性能。
- **任务7：绘制训练曲线** – 展示 loss 和 accuracy 曲线。
- **任务8：结果分析** – 输出过拟合判断、准确率差距等。
- **进阶任务2：比较优化器** – 对比 SGD 和 Adam 的测试准确率。

## 实验结果

- **测试集准确率**：99.17%
- **训练 loss**：从 0.156 降至 0.0143
- **验证 loss**：最终 0.0307
- **训练/验证准确率差距**：0.35%（未过拟合）
- **优化器对比**：Adam (99.03%) vs SGD (98.99%)

日期：2026年5月15日
