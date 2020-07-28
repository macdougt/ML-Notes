# ML-Notes

### Terms

| Term          | Description|
| ------------- |:-------------|
|Softmax|A form of logistic regression that normalizes an input value into a vector of values that follows a probability distribution whose total sums up to 1. |
|One-Hot as defined for encoding| A group of bits among which the legal combinations of values are only those with a single high (1) bit and all the others low (0)      |
|Dropout|The process of randomly disconnecting nodes from the current layer to the next layer. This process of random disconnects naturally helps the network to reduce overfitting as no one single node in the layer will be responsible for predicting a certain class, object, edge, or corner.|
|Max pooling| A sample-based discretization process. The objective is to down-sample an input representation (image, hidden-layer output matrix, etc.), reducing its dimensionality and allowing for assumptions to be made about features contained in the sub-regions binned|
|Batch normalization|A technique for improving the speed, performance, and stability of artificial neural networks and used to normalize the input layer by re-centering and re-scaling|
|Batch Size|A hyperparameter of gradient descent that controls the number of training samples to work through before the model’s internal parameters are updated.|
|Epoch|A hyperparameter of gradient descent that controls the number of complete passes through the training dataset.|
|Masking|Used to indicate to sequence-processing layers that certain timesteps in an input are missing, and thus should be skipped when processing the data.|
|Padding |A special form of masking were the masked steps are at the start or at the beginning of a sequence. Padding comes from the need to encode sequence data into contiguous batches: in order to make all sequences in a batch fit a given standard length, it is necessary to pad or truncate some sequences.|
|Long short-term memory (LSTM)|Artificial recurrent neural network (RNN) architecture that has feedback connections. It can process both single data points (such as images), and entire sequences of data (such as speech or video). The expected input structure has 3 dimensions [samples, [timesteps](https://stackoverflow.com/a/54236050), features].|
|Bidirectional LSTM|2 LSTMs are trained on the input sequence. The first on the input sequence as-is and the second on a reversed copy of the input sequence.|
|TimeDistributed wrapper layer|Wraps output layer so that one value per timestep can be predicted given the full sequence provided as input. This requires that the LSTM hidden layer returns a sequence of values (one per timestep) rather than a single value for the whole input sequence.|
|Rectified Linear Unit (ReLU)|The rectifier is an activation function defined as the positive part of its argument (i.e. f(x) = max(0,x)|
|Leaky ReLU|f(x) = x, if x > 0 and 0.01x otherwise|

[Calculating Number of Parameters in a LSTM Unit & Layer](https://medium.com/@priyadarshi.cse/calculating-number-of-parameters-in-a-lstm-unit-layer-7e491978e1e4)


### GAN (Generative Adversarial Network)

A GAN is comprised of 2 models (a discriminator and a generator)

A generator takes input in the form of a vector of random numbers (called latent space) and generates an output (e.g. an image).

Convolution networks downsample an image to a set of features. The generator will do the opposite and upsample from a set of features to generate an image. Keras exposes the Conv2DTranspose layer to help with this task. Both the Conv2D (used in convolution) and Conv2DTranspose layers use the strides parameter as contraction and expansion factor in their tranformation.


