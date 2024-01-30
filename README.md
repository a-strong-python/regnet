# Regnet

## 介绍

以下是我们在论文 **“设计网络设计空间”** 中描述的网络设计范式的 pytorch 实现

[![](https://github.com/a-strong-python/regnet/raw/master/demo/x1.png)](https://github.com/a-strong-python/regnet/blob/master/demo/x1.png)  
                                                                    _设计空间设计_



## 比较

P：论文的。O：我们的

| 型                | \[P/O\] gflops | \[P/O\] 参数 | \[P/O\] top-1 错误 |
| ----------------- | -------------- | ------------ | ------------------ |
| RerNetY-200MF系列 | 0.2/0.22       | 3.2/3.27     | 29.6/更新中...     |
| RerNetY-400MF系列 | 0.4/0.42       | 4.3/4.45     | 25.9/更新中...     |
| RerNetY-600MF系列 | 0.6/0.60       | 6.1/5.66     | 24.5/更新中...     |
| RerNetY-800MF系列 | 0.8/0.82       | 6.3/6.26     | 23.7/更新中...     |



## 最佳模型

[![](https://github.com/a-strong-python/regnet/raw/master/demo/x29.png)](https://github.com/a-strong-python/regnet/blob/master/demo/x29.png)   
                                                                    _热门 RegNetX 型号_



[![](https://github.com/a-strong-python/regnet/raw/master/demo/x30.png)](https://github.com/a-strong-python/regnet/blob/master/demo/x30.png)  
                                                                     _热门 RegNetY 型号_



## 数据

**如论文所述，我们使用 Imagenet（ILSVRC2012）进行所有实验。**

在此存储库下创建一个数据文件夹，

```
cd {repo_root}
mkdir data
```

- **ImageNet**： 下载 ImageNet 数据集，并将文件按以下结构放置： 当然，您可以根据自己的喜好将此路径更改为您想要的任何路径，或者在使用 docker 时将其挂载到文件夹中。

  ```
  data
  ├── train
  │   ├── n01440764
  │   └── n01443537
  │   └── ...
  │── val
  │   ├── n01440764
  │   └── n01443537
  │   └── ...
  ```



## 如何使用我们的代码

使用我们的代码，您可以：

-   通过运行 **python train.py -d path/to/image/root/folder**，使用默认参数**训练模型**
-   我们还提供了 shell 脚本，可用于在 **./scripts/** 中运行第一个 RegnetY 模型的训练。例如，如果你想训练RegNetY 800MF，你可以简单地运行**./scripts/RegnetY\_800MF.sh**



## 要求

-   **python 3.7**
-   **pytorch 1.4**
-   **opencv (cv2)**
-   **pthflops**
-   **torchsummary**



## 更新 （21/04/2020）

完成所有网络和训练脚本。我们正在训练RegnetY模型，并将很快更新结果。



## 引用

-   [facebookresearch/pycls](https://github.com/facebookresearch/pycls)
-   [pytorch/examples](https://github.com/pytorch/examples)

