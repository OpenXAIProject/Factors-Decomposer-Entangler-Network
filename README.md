# FDEN
A COMPACT AND LEGIBLE SOURCE CODE IS COMING!  
Implementation of [Plug-in Factorization for Latent Representation Disentanglement](https://arxiv.org/abs/1905.11088).

### Requirements
Tensorflow (2.0.0-alpha0)  
Pillow

### Data sets
1. [Omniglot](https://github.com/brendenlake/omniglot)  
Download [omniglot/python/images_background.zip](https://github.com/brendenlake/omniglot/raw/master/python/images_background.zip) and [omniglot/python/images_evaluation.zip](https://github.com/brendenlake/omniglot/raw/master/python/images_evaluation.zip).  
Place them into **data/raw/omniglot/** folder.
2. Mini-ImageNet  
Download  [ImageNet](http://image-net.org/download-images) and rename it to images.zip.  
Download [index files](https://github.com/twitter/meta-learning-lstm/tree/master/data/miniImagenet).  
Place them into **data/raw/imagenet/** folder.  
3. [Oxford Flower 102](http://www.robots.ox.ac.uk/~vgg/data/flowers/102/index.html)  
Download [images](http://www.robots.ox.ac.uk/~vgg/data/flowers/102/102flowers.tgz) and [labels](http://www.robots.ox.ac.uk/~vgg/data/flowers/102/imagelabels.mat).  
Place them into **data/raw/oxford/** folder.
4. MS-Celeb-1M Low-shot  
NOTE: [Official website](https://webcache.googleusercontent.com/search?q=cache:PYPw2UO9SfEJ:https://www.msceleb.org/download/lowshot%20&cd=1&hl=ko&ct=clnk&gl=kr) is down. Please ask the organizers (Microsoft) for access to the data set.  
Download TrainData_lowshot.tsv, DevelopmentSet.tsv, TrainData_Base.tsv.  
Place them into **data/raw/msceleb/** folder.

### How to run
`python main.py --dataset=0 --mode=100 --way=5 --shot=1`  
Dataset: 0 - Omniglot, 1 - MS-Celeb-1M, 2 - Mini-ImageNet, 3 - Oxford Flower  
Mode:  
Invertible Network: 0## Began, 1## ALI  
Classifier: #0# Siamese Network, #1# Prototypical Network  
Mode: ##0 Train Invertible network, ##1 Train FDEN  
Example: 101 ALI invertible network + Siamese + train FDEN  
Way, shot: C-way K-shot learning setting for training FDEN

#### settings.py
root_path: Root path  
project_path: Source code path  
raw_data_path: Raw data set path (~36GB)  
preprocessed_data_path: Path to store preprocessed data (~110GB)  
temp_data_path: Path to store temporary data (~115GB)  
result_path = Path to save results (tensorboard event files, model weights, source code)

## Acknowledgement

<img src="http://xai.unist.ac.kr/static/img/logos/XAIC_logo.png" width="300" height="100">

### **Project Name**
> A machine learning and statistical inference framework for explainable artificial intelligence(의사결정 이유를 설명할 수 있는 인간 수준의 학습·추론 프레임워크 개발)

### **Managed by**
> Ministry of Science and ICT/XAIC

### **Participated Affiliation**
> UNIST, Korea Univ., Yonsei Univ., KAIST., AItrics

### **Web Site**
> <http://openXai.org>

### LICENSE
> This data is made available under the Creative [Commons CC BY-SA 3.0 license](https://creativecommons.org/licenses/by-sa/3.0/legalcode).
