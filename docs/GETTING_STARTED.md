# Getting Started

This document provides install instructions and basic usage examples of the Hailo Model Zoo.

## System Requirements

- Ubuntu 18.04, Python 3.6
- The Hailo Model Zoo has been tested with Hailo Dataflow Compiler v3.9 (Obtain from [**hailo.ai**](http://hailo.ai)).
- The Hailo Model Zoo currently does not support running on CPU; a GPU system is required.
- The Hailo Model Zoo supports Hailo-8 connected via PCIe only.

## Install Instructions

1. Install the Hailo Dataflow compiler and enter the virtualenv (visit [**hailo.ai**](http://hailo.ai) for further instructions).
2. Clone this repo:
```
git clone https://github.com/hailo-ai/hailo_model_zoo.git
```
3. run the setup script:
```
cd hailo_model_zoo; pip install -e .
```
4. For setting up datasets please see [**DATA.md**](DATA.md).
5. Verify Hailo-8 is connected through PCIe (required only to run on Hailo-8. Full-precision / emulation run on GPU.)
```
hailo fw-control identify
```
Expected output:
```
Identifying board
Control Protocol Version: 2
Firmware Version: 2.9.0 (release,app)
Logger Version: 0
Board Name: Hailo-8
```

## Usage

### Flow Diagram
The following scheme shows highlevel view of the model-zoo evaluation process, and the different stages in between.

<p align="center">
  <img src="images/usage_flow.svg" />
</p>

### Evaluation

The pre-trained models are stored on AWS S3 and will be downloaded automatically when running the model zoo.
To evaluate models in full precision:
```
python hailo_model_zoo/main.py eval <model_name>
```
To evaluate models with the Hailo emulator (after quantization to integer representation - fast_numeric):
```
python hailo_model_zoo/main.py eval <model_name> --target emulator
```
To evaluate models on Hailo-8:
```
python hailo_model_zoo/main.py eval <model_name> --target hailo8
```
To limit the number of images for evaluation use the following flag:
```
python hailo_model_zoo/main.py eval <model_name> --eval-num <num-images>
```
To explore other options (for example: changing the default batch-size) use:
```
python hailo_model_zoo/main.py eval --help
```

### Parsing
To parse models into Hailo's internal representation and generate the Hailo Archive (HAR) file:
```
python hailo_model_zoo/main.py parse <model_name>
```

### Quantize
To quantize models from full precision into integer representation and generate a quantized Hailo Archive (HAR) file:
```
python hailo_model_zoo/main.py quantize <model_name>
```

### Profiling
To generate the Hailo profiler report:
```
python hailo_model_zoo/main.py profile <model_name>
```

### Compile
To run the Hailo compiler and generate the Hailo Executable Format (HEF) file:
```
python hailo_model_zoo/main.py compile <model_name>
```

### Visualization
To run visualization (without evaluation) and generate the output images:
```
python hailo_model_zoo/main.py eval <model_name> --visualize
```
To create a video file from the network predictions:
```
python hailo_model_zoo/main.py eval <model_name> --visualize --video-outpath /path/to/video_output.mp4
```

## Citation

The Hailo quantization scheme includes the following papers:

```
@InProceedings{Finkelstein2019,
  title = {Fighting Quantization Bias With Bias},
  author = {Alexander Finkelstein and Uri Almog and Mark Grobman},
  booktitle = {CVPR},
  year = {2019}
}
@InProceedings{Meller2019,
  title = {Same, Same But Different - Recovering Neural Network Quantization Error Through Weight Factorization},
  author = {Eldad Meller and Alexander Finkelstein and Uri Almog and Mark Grobman},
  booktitle = {ICML},
  year = {2019}
}
```