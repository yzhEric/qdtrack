# Quasi-Dense Instance Similarity Learning


We present a [trailer](https://youtu.be/o8HRJAOZidc) that consists of method illustrations and tracking visualizations. Take a look!


## Abstract

Similarity metrics for instances have drawn much attention, due to their importance for computer vision problems such as object tracking. However, existing methods regard object similarity learning as a post-hoc stage after object detection and only use sparse ground truth matching as the training objective. This process ignores the majority of the regions on the images. In this paper, we present a simple yet effective quasi-dense matching method to learn instance similarity from hundreds of region proposals in a pair of images. In the resulting feature space, a simple nearest neighbor search can distinguish different instances without bells and whistles. When applied to joint object detection and tracking, our method can outperform existing methods without using location or motion heuristics, yielding almost 10 points higher MOTA on BDD100K and Waymo tracking datasets. Our method is also competitive on one-shot object detection, which further shows the effectiveness of quasi-dense matching for category-level metric learning. 



## Quasi-dense matching
![teaser](figures/teaser.png)


## Installation

### Requirements

- Linux
- Python 3.6+ 
- PyTorch 1.3+
- CUDA 9.2+ (If you build PyTorch from source, CUDA 9.0 is also compatible)
- NCCL 2+
- GCC 5+
- [mmcv](https://github.com/open-mmlab/mmcv)
- [mmdet](https://github.com/open-mmlab/mmdetection)

### Install 

a. Create a conda virtual environment and activate it.
```shell

conda create -n qdtrack python=3.7 -y
conda activate qdtrack
```

b. Install mmcv and mmdetection, see [offical instructions](https://github.com/open-mmlab/mmdetection/blob/master/docs/install.md).

```shell
pip install mmcv-full

# Please find another path to compile mmdetection
git clone https://github.com/open-mmlab/mmdetection.git
cd mmdetection
python setup.py develop
```

c. Install qdtrack
```shell
python setup.py develop
```

### Run QDTrack
The config files are in the folder `configs`.
The running instruction follows [here](https://github.com/open-mmlab/mmdetection/blob/master/docs/getting_started.md).



## Citation 

```
@article{pang2020quasi,
  title={Quasi-Dense Instance Similarity Learning},
  author={Pang, Jiangmiao and Qiu, Linlu and Chen, Haofeng and Li, Qi and Darrell, Trevor and Yu, Fisher},
  journal={arXiv preprint arXiv:2006.06664},
  year={2020}
}
```