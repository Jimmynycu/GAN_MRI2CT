# GAN_MRI2CT

This is a summer intern project in ITRI 2024

The different file is a implementation from :

[Cycle GAN](https://arxiv.org/abs/1703.10593)

[WGAN](https://arxiv.org/abs/1701.07875)

[Leveraging Multimodal CycleGAN for the Generation of Anatomically Accurate Synthetic CT Scans from MRIs](https://www.arxiv.org/abs/2407.10888)

The codes are all modified from github or tensorflow public code base.

## Setup


### Env
- Tensorflow 2.17

### Recommended
- Linux with Tensorflow GPU edition

### Getting Started

Create Docker Image

```sh
docker run -i tensorflow/tensorflow:2.17.0rc1-gpu-jupyter bash
```
Git Clone Repo
```sh
git clone https://github.com/Jimmynycu/GAN_MRI2CT.git
```

Install Package
```sh
pip install -r requirements.txt
```

### Modify Code

## Dataset Prepare
The code require training data image and test data image being arranged into structured file path

```
├── Train
│   ├── MR_Train
│   └── CT_Train
└── Test
    ├── MR_Test
    └── CT_Test
```

## Code 

### Modify Dataset Path
```
test_mr  = tf.data.Dataset.list_files(str('$Your MR Path'), shuffle=True)
test_ct  = tf.data.Dataset.list_files(str('$Your CT Path'), shuffle=True)
```


