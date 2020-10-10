# Skoltech.HackLab.Sbermarket

# Deep Learning for Next Basket Recommendation

This repository contains implementations of [DREAM](http://www.nlpr.ia.ac.cn/english/irds/People/sw/DREAM.pdf) for next basket prediction.

## Requirements

- Python 3.6
- Pytorch 1.6.0
- Pandas 1.1.2
- Sklearn 0.19.1
- Numpy 1.16.2
- Gensim 3.5.0
- Tqdm 4.49.0 

## Data

You can download the [Data.csv](https://drive.google.com/file/d/11CV9-8jKusG1XZj5vqa_rAKAxal1Sorq/view?usp=sharing) used in code.

### Data Format


## Network Structure

DREAM uses RNN to capture sequential information of users' shopping behavior. It extracts users' dynamic representations and scores user-item pair by calculating inner products between users' dynamic representations and items' embedding.

![](https://live.staticflickr.com/65535/49612979743_33d836d5a4_o.png)

The framework of DREAM:

1. Pooling operation on the items in a basket to get the representation of the basket. 
2. The input layer comprises a series of basket representations of a user. 
3. The dynamic representation of the user can be obtained in the hidden layer.
4. The output layer shows scores of this user towards all items.

References:

> Yu, Feng, et al. "A dynamic recurrent model for next basket recommendation." Proceedings of the 39th International ACM SIGIR conference on Research and Development in Information Retrieval. ACM, 2016.
