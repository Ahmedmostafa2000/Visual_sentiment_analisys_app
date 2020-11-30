# updates soon:
- readme update
- finetuning last two layers for better accuracy
- investing the lack of disgust data instances
- investigating overfit

# required libraries
- keras

# model specifications
- This model was created with Mobilnet v2 as base model
  - MobilNet V2 uses depthwise separable convolution, so it has 3 million parameters and can reach the performance of a network with x10 parameters
  - The base model is 14 MB due its small parameters numbers, so it fits on a mobile phone and doesn't take much ram to work[paper](https://arxiv.org/pdf/1804.10892.pdf)
- I added a dense layer after the base model as it raised accuracy

# data
I used FER_2013 data from kaggle [dataset](https://www.kaggle.com/msambare/fer2013) with 65% of data for training, 15% for developement, and 20% for testing


# Results
99% on training data, 65% on validation, 64% on testing data regarding that the state of the art is 75% ([paper](https://arxiv.org/pdf/1804.10892.pdf#:~:text=With%20a%20top%20ac%2D%20curacy,the%20best%20accuracy%20of%2087.76%25.))
