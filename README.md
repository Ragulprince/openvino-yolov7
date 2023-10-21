# Pothole Detection Showdown: YOLOv7 Native vs. Intel OneAPI

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

![YOLO Native - FP32](https://github.com/Ragulprince/dummy/assets/94695130/ed815ca3-7335-4117-af35-b71a5ada4e17)


![OPENVINO - INT8](https://github.com/Ragulprince/dummy/assets/94695130/8d628461-ff20-4531-8f58-1f4ebfc92d5d)

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
  git clone https://link-to-project
```

Open the Jupyter Notebook File

```bash
  OneAPI-Optimised.ipynb
```

Run all the cells

```bash
  Desired Output
```



