# Pothole Detection Showdown: YOLOv7 Native vs. Intel OneAPI

#INTEL ONEAPI

What is Intel OneAPI?

Intel OneAPI is a comprehensive software stack developed by Intel that redefines the way we harness the power of diverse computing architectures for a wide range of workloads, including artificial intelligence and deep learning tasks. Its fundamental mission is to enable developers to create high-performance, cross-architecture applications with ease.

How Does It Work?

At its core, Intel OneAPI provides developers with a unified programming model that simplifies the process of creating applications that can run efficiently on a variety of Intel processors, GPUs, FPGAs, and other hardware accelerators. It is designed to abstract the complexities of the underlying hardware, allowing developers to focus on their application logic rather than the intricacies of specific architectures.

Motto of Intel OneAPI

The guiding motto of Intel OneAPI is "One API, One Language, One Stack." This encapsulates the essence of the project, emphasizing a singular, consistent interface for developers to target a multitude of Intel architectures. By providing a unified and consistent approach to software development, Intel OneAPI simplifies the path to high-performance, multi-architecture applications, ultimately bridging the gap between software and hardware.

##LIBARIES USED

OpenVINO

OpenVINO, short for Open Visual Inference and Neural network Optimization, is the crown jewel within the Intel OneAPI Libraries. This toolkit serves as the linchpin in our pursuit of real-time pothole detection with unparalleled efficiency. OpenVINO excels at optimizing and deploying deep learning models across a spectrum of Intel hardware, ensuring peak performance. Not only did OpenVINO amplify our processing power, but it also simplified the intricate process of model conversion, streamlining our YOLOv7 implementation for Intel's architecture. Additionally, OpenVINO's integration with the Neural Network Compression Framework (NNCF) facilitated post-quantization, resulting in enhanced model efficiency. Through OpenVINO, we unlocked the true potential of our pothole detection system, making it a powerful and agile solution that transcends traditional boundaries.


Project Description:
In this project, we conducted a head-to-head comparison between two powerful object detection approaches, YOLOv7 native and Intel OneAPI Libraries, in the context of pothole detection. 🕳️

📌 Objective: Our goal was to determine which approach offered the best trade-off between processing power and accuracy for real-time pothole detection. 

🚀 Highlights: Implemented YOLOv7 for pothole detection using PyTorch. Leveraged Intel OneAPI Libraries, achieving a surprising twofold increase in processing power. Conducted comprehensive validation and model conversion steps. Post-quantization with NNCF for enhanced efficiency.


## Roadmap

- Get Pytorch model
- Prerequisites
- Check model inference
- Export to ONNX
- Convert ONNX Model to OpenVINO Intermediate Representation (IR)
- Verify model inference
  - Preprocessing
  - Postprocessing
  - Select inference device
- Verify model accuracy
  - Download dataset
  - Create dataloader
  - Define validation function
- Optimize model using NNCF Post-training Quantization API
- Validate Quantized model inference
- Validate quantized model accuracy
- Compare Performance of the Original and Quantized Models



## Screenshots

YOLOV7 Native
![FP32](https://github.com/Ragulprince/openvino-yolov7/assets/94695130/42246cfe-bf35-44e3-a102-ba4609de14ab)

INTEL ONEAPI-OPENVINO
![INT8](https://github.com/Ragulprince/openvino-yolov7/assets/94695130/36bfc243-ee82-4dfc-963f-31376c60a3c4)



## Conclusion

In the context of YOLOv7 or other object detection models, INT8 quantization can significantly improve inference speed and reduce model size without sacrificing much accuracy, making it a practical choice for many real-time applications.


## Result
**Laptop Specifications**:
- MODEL: ACER PREDATOR HELIOS 300 🖥️
- RAM: 16 GB 📶
- Shared GPU: Intel UHD Graphics (8 GB) 🖥️
- Dedicated GPU: NVIDIA RTX 3060 (6 GB) 🎮

**Before oneAPI (FP32) 💻**:
- Average inference time: 908.05 ms ⏱️
- Minimum inference time: 301.41 ms ⏱️
- Maximum inference time: 19203.12 ms ⏱️
- Throughput: 4.40 FPS 🚀

**After oneAPI (INT8) 💥**:
- Average inference time: 444.06 ms ⏱️
- Minimum inference time: 343.21 ms ⏱️
- Maximum inference time: 635.26 ms ⏱️
- Throughput: 9.00 FPS 

**Analysis 📊**:
- The average inference time after using oneAPI (INT8) is approximately half of the average inference time before (FP32), indicating a significant improvement in inference speed. 🚀
- The minimum and maximum inference times also show a noticeable reduction after applying oneAPI, resulting in more consistent and faster inference times. 💨
- The throughput, measured in frames per second (FPS), appears to have increased after using oneAPI, suggesting improved real-time performance. 📈

These optimizations are particularly valuable for real-time computer vision applications, making your laptop more capable for such tasks. 👏👁️🔍🚀

## Acknowledgements

The information and guidance in this report were referenced from the [OpenVINO Notebooks Repository](https://github.com/openvinotoolkit/openvino_notebooks/tree/main/notebooks/226-yolov7-optimization). We extend our gratitude to the contributors and authors of the repository for their valuable insights and resources that contributed to this work.


## Run Locally

Clone the project

```bash
  git clone https://github.com/Ragulprince/openvino-yolov7
```

Open the Jupyter Notebook File

```bash
  OneAPI-Optimised.ipynb
```

Run all the cells

```bash
  Desired Output
```



