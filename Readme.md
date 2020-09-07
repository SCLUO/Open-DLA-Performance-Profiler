## Open-DLA-Performance-Profiler

Portable (Windows) performance profiler for deep neural network. Give you the performance guideline of the model running on different openDLA architectures.

The **openDLA** is based on the open project [**NVDLA**](http://nvdla.org/index.html).

This tool is developed based on [**netron**](https://github.com/lutzroeder/netron).

### Usage
 1. Load the DLA architecture from the directory, select some architectures
 2. Load a model description of Caffe prototxt format
 3. click [view] and select summary, traffic, and detail tables
 4. explore the raw data
 5. copy raw data to your preferal spreadsheet tool to plot trends

### Key Words
- Summary Table :  Summary of cycle counts, FPS of the model
  - MAC Utilization: average MAC utilization under aggressive FPS
  - Roofline Factor: the ratio of memory access cycles / total cycles
  - Conservative FPS: consider the memory access and computation is fully overlapped 
  - Aggressive FPS: consider the memory access and computation is fully interleaved

- Traffic Table : List of the memory traffic of each layer
  - IFM	: input feature map
  - OFM	: output feature map
  - WM : weight matrix

- Detail Table : List of the fused layers based on openDLA
  - type	:  computation type
  - attributes	: 	fused layers
  - ch_in	: input channel number
  - dim_in	: 	input dimension
  - ch_out	: 	output channel number
  - kernel_w	: 	kernel width
  - kernel_h	: 	kernel height
  - pad_w	: padding size of width direction
  - pad_h	: padding size of height direction
  - stride_w	:  stride size of width direction
  - stride_h	:  stride size of height direction
  
  
---------------------------------

### Deferences between the free version here and commercial version

| Features | Free Version (here) | Commercial Version |
| ------   | -----------  | ------------------ |
| Layer Fuse Info  | O | O |
| Performance Table w/ DRAM          | O | O |
| Performance Table w/ SRAM + DRAM   | X | O |
| DRAM/SRAM access policy | X | O |
| DRAM data footprint | O | O |
| DRAM/SRAM data footprint | X | O |
| Configurable Freq./MEM BW | X | O |
| Model Format | Caffe | ONNX, TensorFlow, Caffe...|
| Source Codes | X | Available |
