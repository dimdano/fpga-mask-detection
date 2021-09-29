# fpga-mask-detection
Mask Detection on faces using Xilinx DPU in embedded FPGAs

<img src="cover.png" width="332" height="274">

fpga-mask-detection is a Deep Learning project that implements a face mask detection algorithm based on Convolutional Neural Networks. The model is trained on Tensorflow and then quantized and compiled using Xilinx Vitis AI in order to run on Xilinx DPU of MPSoC FPGAs. The model runs fast on the hardware with little accuracy drop due to quantization. The project was based on [this](https://github.com/altaga/Facemask-Detector-ZCU104 "Named link title") repo. 

## System requirements

- Ubuntu Linux on host pc (18.04 recommended)
- Docker installed on host pc
- Vitis AI 1.2 installed on host pc
- MPSoC ZCU104 configured with Pynq SD-card image 2.6
- DPU-PYNQ v1.2 installed on MPSoC board
- SSH connection to board and remote Jupyter Notebook  

## Running the project

Two Notebooks are provided.

The train-compile notebook must run through Vitis AI. It trains the model on the dataset provided and creates the model "executable" to run on Xilinx ZCU104 DPU.

The test-model notebook must run on board and it executes the whole application from loading the required DPU binaries to the CNN inference for face mask detection.


## Contact

Dimitrios Danopoulos: dimdano@microlab.ntua.gr
