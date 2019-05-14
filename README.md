# caffe-mobilenet-v3
### Introduction
This is a personal Caffe implementation of MobileNetV3. For details, please read the original papers: [Searching for MobileNetV3](https://arxiv.org/pdf/1905.02244.pdf).

### How to use
1. Requirements for `Caffe` (see: [Caffe installation instructions](http://caffe.berkeleyvision.org/installation.html))
2. Add new caffe layers and rebuild the caffe:
	- **Depthwise Convolutional Layer** from [yonghenglh6/DepthwiseConvolution](https://github.com/yonghenglh6/DepthwiseConvolution) 
	- **ReLU6 Layer** from [RuiminChen/Caffe-MobileNetV2-ReLU6](https://github.com/RuiminChen/Caffe-MobileNetV2-ReLU6) 
3. Run test
	```Shell
	CPU:
	$CAFFE_ROOT/build/tools/caffe time -model mobilenet_v3_large_1.0.prototxt
	GPU:
	$CAFFE_ROOT/build/tools/caffe time -model mobilenet_v3_large_1.0.prototxt -gpu 0
	```

### Performance on MobileNetV3
| Backbone            | CPU-Forward | CPU-Backward | GPU-Forward | GPU-Backward |
| ------------------- |:---------:  | :---------:  | :---------: | :---------:  |
| V3-Large 1.0        |  134.55 ms  |  140.23 ms   |  15.44 ms   |   21.79 ms   |
| V3-Small 1.0        |  58.64  ms  |  59.30  ms   |  11.49 ms   |   12.58 ms   |


### TODO
 - More MobileNetV3 architectures.
 - Traning & validation.




