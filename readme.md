# RLGrid: Reinforcement Learning Controlled Grid Deformation for Coarse-to-Fine Point Could Completion

This repository contains PyTorch implementation for **RLGrid: Reinforcement Learning Controlled Grid Deformation for Coarse-to-Fine Point Could Completion.**

RLGrid is a network that leverages reinforcement learning for 2D Grid Scale selection and can be plug-and-play on any operation that uses 2D Grid for coarse-to-fine completion.

### Network

![Net](https://github.com/MarkLiSS/RLGrid/blob/master/images/Net.jpg)


### Usage

Pytorch >= 1.7.0

python >= 3.7

CUDA >= 11.0

GCC >= 4.9

tensorboardX

open3d

pyntcloud

> conda create --name RLGrid --file requirements.txt



#### Building Pytorch Extensions for Chamfer Distance, Earth Mover's Distance 

*NOTE:* PyTorch >= 1.7 and GCC >= 4.9 are required.

> \#Chamfer Distance
>
> cd utils/Chamfer_dist
>
> python setup.py install



> \#Earth Mover's Distance
>
> cd utils/EMD
>
> python setup.py install



### Dataset

The details of used datasets can be found in [DATASET.md](https://github.com/I2-Multimedia-Lab/RLGrid/blob/master/dataset/readme.md).



### Training

To train a point cloud completion model from scratch, run:

```python
#train AE
python train_AE.py
```

```python
#train sc-GAN
python pretrain_treegan.py
```

```python
#train RL Agent
python train_RL_Agent.py
```

### Visualization

Some Results on PCN Dataset

![results](https://github.com/MarkLiSS/RLGrid/blob/master/images/results.jpg)

Some intermediate process (The green box represents that the better coarse output is generated by sc-GAN, while the blue box represents that the better coarse output is generated by AE.)

![IP](https://github.com/MarkLiSS/RLGrid/blob/master/images/IP.jpg)
