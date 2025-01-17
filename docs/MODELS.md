# Pre-Trained Models

Here, we give the full list of models supported by the Hailo Model Zoo.
- FLOPs in the table are counted as MAC operations.
- Networks available in [**TAPPAS**](https://hailo.ai/developer-zone/tappas-apps-toolkit/) are marked with :star:

## Classification

### ImageNet

| Network Name | Top-1 | Input Resolution (HxWxC) | Params (M) | FLOPs (G) | Source |
| -------------- | ------------------------- | ------------------------ | ---------- | --------- | ---- |
| efficientnet_l | 80.47 | 300x300x3 | 9.01 | 9.68 | [**link**](https://github.com/tensorflow/tpu/tree/master/models/official/efficientnet/edgetpu) |
| efficientnet_m | 78.98 | 240x240x3 |5.58 | 3.67 | [**link**](https://github.com/tensorflow/tpu/tree/master/models/official/efficientnet/edgetpu) |
| efficientnet_s | 77.61 | 224x224x3 | 4.13 | 2.36 | [**link**](https://github.com/tensorflow/tpu/tree/master/models/official/efficientnet/edgetpu) |
| efficientnet_lite0 | 74.93 | 224x224x3 | 3.35 | 0.39 | [**link**](https://github.com/tensorflow/tpu/tree/master/models/official/efficientnet/lite) |
| efficientnet_lite1 | 76.66 | 240x240x3 | 4.11 | 0.60 | [**link**](https://github.com/tensorflow/tpu/tree/master/models/official/efficientnet/lite) |
| efficientnet_lite2 | 77.44 | 260x260x3 | 4.78 | 0.86 | [**link**](https://github.com/tensorflow/tpu/tree/master/models/official/efficientnet/lite) |
| efficientnet_lite3 | 79.2  | 280x280x3 | 6.88 | 1.39 | [**link**](https://github.com/tensorflow/tpu/tree/master/models/official/efficientnet/lite) |
| efficientnet_lite4 | 80.64 | 300x300x3 | 11.67 | 2.56 | [**link**](https://github.com/tensorflow/tpu/tree/master/models/official/efficientnet/lite) |
| inception_v1 | 69.76 | 224x224x3 | 5.59 | 1.5 | [**link**](https://github.com/tensorflow/models/tree/v1.13.0/research/slim) |
| mobilenet_v1 | 71.02 | 224x224x3 | 3.2 | 0.57 | [**link**](https://github.com/tensorflow/models/tree/v1.13.0/research/slim) |
| mobilenet_v2_1.0 | 71.84 | 224x224x3 | 2.21 | 0.31 | [**link**](https://github.com/tensorflow/models/tree/v1.13.0/research/slim) |
| mobilenet_v2_1.4 | 74.11 | 224x224x3 | 4.29 | 0.59 | [**link**](https://github.com/tensorflow/models/tree/v1.13.0/research/slim) |
| mobilenet_v3 | 72.27 | 224x224x3 | 2.79 | 1.0 |  [**link**](https://github.com/tensorflow/models/tree/master/research/slim/nets/mobilenet) |
| mobilenet_v3_large_minimalistic | 72.29 | 224x224x3 | 1.4 | 0.21 |  [**link**](https://github.com/tensorflow/models/tree/master/research/slim/nets/mobilenet) |
| regnetx_1.6gf | 77.07 | 224x224x3 | 8.26 | 1.61 | [**link**](https://github.com/facebookresearch/pycls) |
| regnetx_800mf | 75.07 | 224x224x3 | 6.57 | 0.80 | [**link**](https://github.com/facebookresearch/pycls) |
| regnety_200mf | 70.32 | 224x224x3 | 3.15 | 0.2 | [**link**](https://github.com/facebookresearch/pycls) |
| resnet_v1_18 | 68.84 | 224x224x3 | 11.17 | 1.82 | [**link**](https://pytorch.org/vision/0.8/models.html) |
| resnet_v1_34 | 72.68 | 224x224x3 | 21.28 | 3.67 | [**link**](https://github.com/tensorflow/models/tree/v1.13.0/research/slim) |
| resnet_v1_50:star: | 75.21 | 224x224x3 | 23.48 | 3.49 | [**link**](https://github.com/tensorflow/models/tree/v1.13.0/research/slim) |
| resnet_v2_18 | 69.58 | 224x224x3 | 11.17 | 1.82 | [**link**](https://github.com/tensorflow/models/tree/v1.13.0/research/slim) |
| resnet_v2_34 | 73.10 | 224x224x3 | 21.28 | 3.67 | [**link**](https://github.com/tensorflow/models/tree/v1.13.0/research/slim) |
| resnext26_32x4d | 76.08 | 224x224x3 | 13.33 | 2.51 | [**link**](https://github.com/osmr/imgclsmob/tree/master/pytorch) |
| resnext50_32x4d | 79.43 | 224x224x3 | 22.96 | 4.29 | [**link**](https://github.com/osmr/imgclsmob/tree/master/pytorch) |
| shufflenet_g8_w1 | 66.29 | 224x224x3 | 0.92 | 0.18 | [**link**](https://github.com/osmr/imgclsmob/tree/master/pytorch) |
| squeezenet_v1_1 | 59.88 | 224x224x3 | 1.24 | 0.39 | [**link**](https://github.com/osmr/imgclsmob/tree/master/pytorch) |

## Object Detection

### COCO

| Network Name | mAP | Input Resolution (HxWxC) | Params (M) | FLOPs (G) | Source |
| -------------- | ------------------------- | ------------------------ | ---------- | --------- | --- |
| centernet_resnet_v1_18 | 26.37 | 512x512x3 | 14.23 | 	15.73 | [**link**](https://cv.gluon.ai/model_zoo/detection.html) |
| ssd_mobiledet_dsp:star: | 28.9 | 320x320x3 | 	7.07 | 2.83 | [**link**](https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/tf1_detection_zoo.md) |
| ssd_mobilenet_v1:star: | 23.18 | 300x300x3 | 	6.79 | 1.25 | [**link**](https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/tf1_detection_zoo.md) |
| ssd_mobilenet_v1_hd | 17.67 | 720x1280x3 | 6.81 | 	12.26	 | [**link**](https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/tf1_detection_zoo.md) |
| ssd_mobilenet_v2 | 24.27 | 300x300x3 | 4.46 | 0.76 |  [**link**](https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/tf1_detection_zoo.md) |
| ssd_resnet_v1_18 | 17.68 | 300x300x3 | 16.62 | 	3.54 | [**link**](https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/tf1_detection_zoo.md) |
| tiny_yolov3 | 14.22 | 416x416x3 | 8.85 | 	2.79 | [**link**](https://github.com/mystic123/tensorflow-yolo-v3) |
| tiny_yolov4 | 18.89 | 416x416x3 | 6.05 | 3.46 | [**link**](https://github.com/Tianxiaomo/pytorch-YOLOv4) |
| yolov3:star: | 32.62 | 608x608x3 | 68.79 | 79.17	 |  [**link**](https://cv.gluon.ai/model_zoo/detection.html) |
| yolov3_416:star: | 36.06 | 416x416x3 | 68.79 | 37.06	 |  [**link**](https://cv.gluon.ai/model_zoo/detection.html) |
| yolov4:star: | 42.4 | 512x512x3 | 66.05 | 	47.36 | [**link**](https://github.com/AlexeyAB/darknet/wiki/YOLOv4-model-zoo) |
| yolov5xs* | 32.74 | 512x512x3 | 7.91 | 	5.8 | [**link**](https://github.com/ultralytics/yolov5/releases/tag/v2.0) |
| yolov5s*:star: | 34.36 | 640x640x3 | 7.91 | 	9.06 |  [**link**](https://github.com/ultralytics/yolov5/releases/tag/v2.0) |
| yolov5m*:star: | 41.7 | 640x640x3 | 22.95 | 	27.33 |  [**link**](https://github.com/ultralytics/yolov5/releases/tag/v2.0) |

\* Trained without the SPP block

## Semantic Segmentation

### Cityscapes

| Network Name | mIoU | Input Resolution (HxWxC) | Params (M) | FLOPs (G) | Output Stride | Source |
| -------------- | ------------------------- | ------------------------ | ---------- | --------- | ------------ | ---- |
| fcn8_resnet_v1_18:star: | 66.62 | 1024x1920x3 | 11.2 | 	71.51	 | 32 | [**link**](https://cv.gluon.ai/model_zoo/segmentation.html) |
| fcn8_resnet_v1_22 | 68.11 | 1024x1920x3 | 15.12 | 150.04 | 16 | Internal |
| fcn16_resnet_v1_18 | 	65.54 | 1024x1920x3 | 		11.19 | 71.26	 | 32 | [**link**](https://cv.gluon.ai/model_zoo/segmentation.html) |
| fcn16_resnet_v1_18_8_classes | 76.04 | 1024x1920x3 | 	11.18 | 	71.19 | 32 | [**link**](https://cv.gluon.ai/model_zoo/segmentation.html) |

## Pose Estimation

### COCO

| Pose Estimation | AP | Input Resolution (HxWxC) | Params (M) | FLOPs (G) | Source |
| -------------- | ------------------------- | ------------------------ | ---------- | --------- | ---- |
| centerpose_regnetx_800mf | 44.4 | 512x512x3 | 12.31 | 43.06	| [**link**](https://github.com/tensorboy/centerpose) |
| centerpose_regnetx_1.6gf_fpn:star: | 53.9 | 640x640x3 | 14.36 | 32.71 |  [**link**](https://github.com/tensorboy/centerpose) |