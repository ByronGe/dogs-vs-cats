# dogs-vs-cats
利用深度学习识别图片中的猫狗

利用 keras.applications 中提供的预训练神经网络(VGG16和ResNet50)对图像进行特征提取，再将提取得到的特征向量作为输入来训练一个新的全连接神经网络，以处理“猫狗”分类问题。
该模型经过简单的训练，能实现约99.1%的正确率。

项目是基于python 2.7, keras 2.0.4, tensorflow-gpu-1.1.0完成的，主要用到了以下库：

import os:  os.listdir用于读取文件夹中的文件名，返回一个list

from keras.preprocessing.image import load_img: 用于读取图片

import matplotlib.pyplot as plt: 用于可视化图片

from keras.preprocessing.image import img_to_array, load_img: img_to_array 可将图片转化为array

from graphviz import Digraph: 用于画模型图

from keras.applications.vgg16 import VGG16: 用于导入VGG16预训练模型

from keras.applications.resnet50 import ResNet50: 用于导入ResNet50预训练模型

from keras.applications.imagenet_utils import preprocess_input: 用于导入预处理函数

from keras.models import Model: 用于构建函数式模型

from keras.layers import *: 用于添加layer

from keras.optimizers import SGD, Adadelta: 用于导入模型的优化方法

from keras.preprocessing.image import ImageDataGenerator: 图片生成器，可用于提升数据，构造batch数据

import h5py: 用于保存模型的训练参数
