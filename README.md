# Unet3plus

**简介**  
Unet3plus 是基于 TensorFlow 实现的图像分割网络，适用于医学图像分割、遥感图像分割等任务。

![模型结构图](unet3p_architecture.png)


---

## 使用说明

本项目使用 TensorFlow 框架实现

基于
Ubuntu 20.04.5 LTS

tensorflow==2.13.1

NVIDIA GeForce RTX 3060, 1

主要功能包括模型训练、验证和测试。

---

## 数据集结构

项目默认的数据目录结构如下：

```plaintext
data/
├── train/    # 训练集
│   ├── images/   # 训练图片
│   └── masks/    # 训练标签掩码
└── val/      # 验证集
    ├── images/   # 验证图片
    └── masks/    # 验证标签掩码


请确保数据目录和文件结构与上述保持一致，方便程序自动读取。

---

## 配置文件说明

项目的超参数配置文件位于 `configs/config.yaml`，主要参数如下：

```yaml
HYPER_PARAMETERS:
  EPOCHS: 100          # 迭代次数
  BATCH_SIZE: 16       # 每个 GPU 的批量大小
  LEARNING_RATE: 5e-5  # 学习率
```
---
## 进行训练

pip install -r requirements.txt

python trian.py

```plaintext
like this

Epoch 1: val_activation_dice_coef improved from -inf to 0.56526, saving model to /hy-tmp/unet3p/checkpoint/model_unet3plus_deepsup.hdf5
2000/2000 [==============================] - 729s
