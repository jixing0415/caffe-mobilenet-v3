# caffe-mobilenet-v3
### Introduction
This is a personal Caffe implementation of MobileNetV3. For details, please read the original papers: [Searching for MobileNetV3](https://arxiv.org/pdf/1905.02244.pdf).

### How to use
1.Requirements for `Caffe` (see: [Caffe installation instructions](http://caffe.berkeleyvision.org/installation.html))
2.Copy the Depthwise Convolutional Layer from [yonghenglh6/DepthwiseConvolution](https://github.com/yonghenglh6/DepthwiseConvolution), and rebuil the Caffe.
3.Run test
	```Shell
	CPU:
	$CAFFE_ROOT/build/tools/caffe time -model mobilenet_v3_large_1.0.prototxt
	GPU:
	$CAFFE_ROOT/build/tools/caffe time -model mobilenet_v3_large_1.0.prototxt -gpu 0
	```

### Performance on MobileNetV3
| Backbone      | CPU-Forward | CPU-Backward | GPU-Forward | GPU-Backward |
| ------------------- |:---------:| :---------:| :---------:| :---------:|
| V3-Large 1.0        |   134.86 ms  |   152.11 ms   |  15.88 ms  |    22.15ms   |
| ...                          |               |              |               |       .       |


### TODO
 - More MobileNetV3 architectures.
 - Traning & validation.




