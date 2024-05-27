# ResNet18 Deep Neural Network

Created plane RESNET-18 architecture as defined in the Table 1 of the ResNet paper and trained on the CIFAR-10 dataset. The output of each layer is calculated based on the formula outputsize = ((inputsize − kernel + 2 ∗ padding)/stride) + 1. Then Plotted training and test losses and accuracy over 50 epochs. For permuted dataset, chose a seed to apply the same permutation to all the images and repeated the above same steps to plot the losses and accuracy. The observations from the plotted graphs are that for the normal dataset, the test loss, which is less than 1, and accuracy, which is around 80%, of both optimizers SGD and Adam are almost the same at the end of 50 epochs. With permuted dataset, the performance has depreciated compared to normal dataset i.e., the test loss is around 3.25 with SGD and 1.25 with Adam and the test accuracy is around 50% with both SGD and Adam. This indicates that the model is not robust enough and relies on the specific ordering of the samples present in the training data(possibly overfitting to the original data distribution). In addition to that, we’re trying to use a deep neural network ResNet, which might need a larger dataset since it has a large number of parameters. Possibly training with another dataset might give us more performance or trying out other architectures tailored to the CIFAR-10 characteristics might give good performance with permuted data, which can help in generalizing the model.

## References

Deep residual learning for image recognition https://arxiv.org/abs/1512.03385

Project 1 https://github.com/shotsan/ECEN_740_Project1

Pytorch tutorials https://pytorch.org/tutorials/

Grant Sanderson’s video on Neural Networks

ResNet https://gist.github.com/Modojojo/3bb7578a22ae36dcfa9ebc3032583c1c#file-resnet18-py

MNIST tutorials https://pytorch-lightning.readthedocs.io/en/1.5.10/notebooks/lightning_examples/mnist-hello-world.html

Overview of CNNs https://cs231n.github.io/convolutional-networks/#overview

https://pytorch.org/tutorials/beginner/blitz/cifar10_tutorial.html
