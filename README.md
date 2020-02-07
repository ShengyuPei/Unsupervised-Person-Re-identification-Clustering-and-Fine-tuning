# [Unsupervised Person Re-identification: Clustering and Fine-tuning](https://hehefan.github.io/pdfs/unsupervised-person-identification.pdf)
![](https://github.com/hehefan/Unsupervised-Person-Re-identification-Clustering-and-Fine-tuning/blob/master/images/framework.jpg)

## Setup
All our code is implemented in Keras, Tensorflow (Python). Installation instructions are as follows:
```
pip install --user tensorflow-gpu
pip install --user keras
pip install --user sklearn
```
## Baseline (Fine-tuned ResNet-50)
We provide the fine-tuned models as follows:
1. [Duke](https://drive.google.com/uc?export=download&id=0B7NctsDC2gmLSVlGY01XTDd6LUk) 2. [Market](https://drive.google.com/uc?export=download&id=0B7NctsDC2gmLellBSmptRUFlWkU) 3. [CUHK03](https://drive.google.com/uc?export=download&id=0B7NctsDC2gmLbEZua2RHczBtSWc) 4. [Duke + Market](https://drive.google.com/uc?export=download&id=0B7NctsDC2gmLQlI3eV9XWXRwZ2M) 5. [Duke + CUHK03](https://drive.google.com/uc?export=download&id=0B7NctsDC2gmLdXlJRWxwNUUySlU) 6. [Market + CUHK03](https://drive.google.com/uc?export=download&id=0B7NctsDC2gmLc0NHd2tvdVUxNDQ)

## Progressive Unsupervised Learning (PUL)
![](https://github.com/hehefan/Unsupervised-Person-Re-identification-Clustering-and-Fine-tuning/blob/master/images/demo.jpg)

To reappear Duke -> Market:

1. Rename the above fine-tuned "Duke" model as "0.ckpt", which is treated as original model for PUL;

2. Create directory "checkpoint" under the folder "PUL", and move the original model "0.ckpt" into the "checkpoint";

3. Modify PUL/unsupervised.py or PUL/semi-supervised.py and PUL/evaluate.py to train and evaluate Duke -> Market.

If you find this code useful, consider citing our work:
```
@article{fan18unsupervisedreid,
  author    = {Hehe Fan and Liang Zheng and Chenggang Yan and Yi Yang},
  title     = {Unsupervised Person Re-identification: Clustering and Fine-tuning},
  journal   = {{ACM} Transactions on Multimedia Computing, Communications, and Applications {TOMM}},
  volume    = {14},
  number    = {4},
  pages     = {83:1--83:18},
  year      = {2018},
  doi       = {10.1145/3243316}
}
```
