# Live-Object Tracking using Efficient Vision Transformers

The algorithm implementation is based on:

E.T.Tracker:
https://arxiv.org/pdf/2112.09686.pdf


https://github.com/pblatter/ettrack

Wave-Vit:
https://arxiv.org/pdf/2207.04978.pdf


https://github.com/YehLi/ImageNetModel


CMT-S:
https://arxiv.org/pdf/2107.06263.pdf


https://github.com/ggjy/CMT.pytorch


The architecture of the tracking model utilizes LT-Mobile which passes template and search
frame through a convolutional-based siamese-like backbone network for feature extraction. The
normalized features afterward are fused through a cross-correlation layer. The generated feature
map is passed afterward through two heads: a classification head and a regression head. The heads
are composed of a sequence of convolution layers and self-attention modules. We maintained the
number of self-attention modules and the number of attention heads per attention module to generate
different models with close-enough number of parameters. The only change with the three models
was the attention mechanism. Due to the difference in mechanisms, CMT-based tracker has the size
of 7 million parameters, Exemplar tracker has 9 million parameters while WaveViT-based tracker
contains 12 million parameters


models: 

tracking/basic_model

training loop: 

train.ipynb
