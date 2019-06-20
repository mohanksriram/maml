# maml
Explore the basics of meta-learning using Model-Agnostic Meta-Learning

#### Experiment Setup

N= 20, K=1
- N-way classification:
    - Use N class during test with K-shot learning

- Network Architecture
    - 3x3 convolutions and 64 filters
    - ReLU nonlinearity
    - 2x2 max-pooling
- Dataset
    - Omniglot

#### Dependencies
- Python: v3.7^
- Pytorch: v1.1^

#### Usage:

##### Instructions to run the code:

Clone the maml repo
```
https://github.com/mohankumarSriram/maml.git
```

Clone the dataset repo
```
https://github.com/brendenlake/omniglot.git
```

Setup the dataset within the maml repo
```
cd omniglot/python
unzip images_background.zip
unzip images_evaluation.zip
cd ../../maml
mkdir data
cd data
mkdir images_background images_evaluation

cp -r ../../../omniglot/python/images_background/* images_background/

cp -r ../../../omniglot/python/images_evaluation/* images_evaluation/

```

Run the training loop
```
cd ../../src
./train-omniglot-20way-1shot.sh
```

Visualize the data
```
cd ../notebooks
jupyter notebook omniglot_learning_curves.ipynb
```


#### Tasks to do:
- [ ] Port network layers to latest Pytorch.
- [ ] Performance comparison with 5-way one shot classification
- [ ] Performance comparison with different datasets

#### Attribution
This code is adapted from the original implementation [here](https://github.com/katerakelly/pytorch-maml).
