**<u>Convolution</u>**

Its the process of multiplying the filter values to the entire input image one by one(number depends on filter size) and finding the values of the filter by summing those values.

<u>**Filter / kernel**</u>

Filters are 2d/3d matrices. They have some values which are multiplied to the input image and then summed to give the output. Initially the filters have random values.

**<u>Epoch</u>**

The number of times we train on the input image i.e. the number of times the model(all the convolutional, max pooling layers) are run on the image data.

<u>**1x1 convolution**</u>

It can be used to decrease/increase the number of channels after the max pooling layer. Normally it used to decrease the number of channels.                                                                                                                                Eg (200x200x512) | (1x1x512x32) - (200x200x32)

<u>**3x3 convolution**</u>

Convolution performed by 3x3 matrix(filter). Two 3x3 convolutions are preferred than doing one 5x5 convolution as number of parameters are less in two 3x3.(18 vs 25), also Nvidia has made 3x3 faster.                                                                                                                                                      Eg - 200x200x32 | 3x3x32x64

 <u>**Activation Function**</u>

The summation of the input* weight gives an output. Activation function is the one which decides if the value is above a certain threshold and to send it forward or not.

 <u>**Feature Maps**</u>

A feature map for a layer is what the filters are highlighting for that image. The feature map consists of same number of images as the number of filters. As each filter is focusing on a particular feature(horizontal edge, vertical edge) those get highlighted.

 <u>**Receptive Field**</u>

It is the number of pixels a particular layer is able to view. Types - global and local. Global- receptive field of the entire model from that layer. Local - receptive field of that layer locally.                                                         Eg : 244x244 | 3x3(Layer1) | 3x3(Layer2) | 3x3(Layer3). Global of layer2 - 5x5, local of layer2 - 3x3

 