# Anime Character Face Generator

![cover1-1](https://github.com/benliaowc/anime_face/blob/master/faces/0.jpg)
![cover1-2](https://github.com/benliaowc/anime_face/blob/master/faces/2.jpg)
![cover1-3](https://github.com/benliaowc/anime_face/blob/master/faces/3.jpg)
![cover1-4](https://github.com/benliaowc/anime_face/blob/master/faces/4.jpg)

![cover2-1](https://github.com/benliaowc/anime_face/blob/master/faces/5.jpg)
![cover2-2](https://github.com/benliaowc/anime_face/blob/master/faces/6.jpg)
![cover2-3](https://github.com/benliaowc/anime_face/blob/master/faces/7.jpg)
![cover2-4](https://github.com/benliaowc/anime_face/blob/master/faces/8.jpg)

![cover3-1](https://github.com/benliaowc/anime_face/blob/master/faces/9.jpg)
![cover3-2](https://github.com/benliaowc/anime_face/blob/master/faces/10.jpg)
![cover3-3](https://github.com/benliaowc/anime_face/blob/master/faces/11.jpg)
![cover3-4](https://github.com/benliaowc/anime_face/blob/master/faces/12.jpg)

![cover4-1](https://github.com/benliaowc/anime_face/blob/master/faces/13.jpg)
![cover4-2](https://github.com/benliaowc/anime_face/blob/master/faces/15.jpg)
![cover4-3](https://github.com/benliaowc/anime_face/blob/master/faces/16.jpg)
![cover4-4](https://github.com/benliaowc/anime_face/blob/master/faces/18.jpg)

## Introduction

This is a anime character face generator implemented in Tensorflow.

Given some text descriptions, the model is capable to generate some anime character faces that fit the descriptions.

The model is mixed with conditional Deep Convolutional Generative Adversarial Networks (DCGAN) and Least Squares Generative Adversarial Networks (LSGAN).

## Training Data

The training data are images of anime character faces.

Thay are better to be squared, since those images will be resized to 64*64.

For example:

![example1](https://github.com/benliaowc/anime_face/blob/master/faces/63.jpg)
![example2](https://github.com/benliaowc/anime_face/blob/master/faces/68.jpg)
![example3](https://github.com/benliaowc/anime_face/blob/master/faces/73.jpg)
![example4](https://github.com/benliaowc/anime_face/blob/master/faces/83.jpg)
![example5](https://github.com/benliaowc/anime_face/blob/master/faces/110.jpg)
![example6](https://github.com/benliaowc/anime_face/blob/master/faces/184.jpg)

## Results

|    Description    | Image |
| ---------- | --- |
| blue hair red eyes |  ![result1](https://github.com/benliaowc/anime_face/blob/master/samples/sample_1_1.jpg) |
| pink hair green eyes|  ![result1](https://github.com/benliaowc/anime_face/blob/master/samples/sample_2_1.jpg) |
| black hair yellow eyes |  ![result1](https://github.com/benliaowc/anime_face/blob/master/samples/sample_3_1.jpg) |

## Usage

### Prerequisite

First, put your training data under `./faces`.

Second, please clone [skip-thoughts](https://github.com/ryankiros/skip-thoughts) and put it under `./model/`.

Third, put your Tensorflow model under `./model/DCGAN/` if any.

The directory structure will be `./model/skip-thoughts` and `./model/DCGAN`.

### Train

```bash
python3 DCGAN.py --train
```

### Test (Image Generate)

After executing the following commands, the images will be generated under `./samples`.

```bash
python3 --generate -t [Description File] -n [# image per description]
```

* `[Description File]`: A text file that contains descriptions. See [description.txt](https://github.com/benliaowc/anime_face/blob/master/description.txt) as an example.

* `[# image per description]`: Number of images that will be generated per desciprtion. Recommended number: 1.

## Reference

Thanks to En-Yu Fan, one of the TAs in Machine Learning and Having It Deep and Structured 2017 Spring, National Taiwan University, to collect data.

Due to the storage limit of Github, only 200 pictures are uploaded as samples.

If you want to train a model that can generate high quality pictures, please go find more training data.