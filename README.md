# SRGAN

# Try the Pre-trained Model
A pretrained generator model on the DIV2k dataset is provided in the 'models' directory. It uses 6 inverted residual blocks, with 32 filters in every layer of the generator. 

Upsampling is done via phase shifts in the low resolution space for speed.

To try out the provided pretrained model on your own images, run the following:

```bash
python infer.py --image_dir 'path/to/your/image/directory' --output_dir 'path/to/save/super/resolution/images'
```

# Training
To train, simply execute the following command in your terminal:
```bash
python main.py --image_dir 'path/to/image/directory' --hr_size 384 --lr 1e-4 --save_iter 200 --epochs 10 --batch_size 14
```
Model checkpoints and training summaries are saved in tensorboard. To monitor training progress, open up tensorboard by pointing it to the 'logs' directory that will created when you start training.

### Reference
* [1] [Photo-Realistic Single Image Super-Resolution Using a Generative Adversarial Network](https://arxiv.org/abs/1609.04802)
* [2] https://github.com/tensorlayer/srgan


### Citation

```
@article{tensorlayer2017,
author = {Dong, Hao and Supratak, Akara and Mai, Luo and Liu, Fangde and Oehmichen, Axel and Yu, Simiao and Guo, Yike},
journal = {ACM Multimedia},
title = {{TensorLayer: A Versatile Library for Efficient Deep Learning Development}},
url = {http://tensorlayer.org},
year = {2017}
}
```
