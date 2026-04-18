# Survey on NeRF and 3DGS in Satellite Remote Sensing

## Overview
This repository contains research and documentation related to our survey on **Neural Radiance Fields (NeRF)** and **3D Gaussian Splatting (3DGS)** as applied to satellite remote sensing. As modern satellites capture vast amounts of data, the field is shifting from flat 2D representations to immersive, high-fidelity **3D digital twins** of urban environments and landscapes.

Our survey explores how these two modern techniques overcome the limitations of traditional photogrammetry—such as shifting shadows, atmospheric changes, and massive dataset sizes—to revolutionize 3D reconstruction from space.

---

## Core Technologies

### 1. Neural Radiance Fields (NeRF)
* **Mechanism**: Uses a deep neural network (typically a Multilayer Perceptron) to represent a scene implicitly as a continuous 5D function.
* **Strengths**: Excellent at handling complex reflections, translucency, and lighting changes.
* **Satellite Adaptation**: Models like **S-NeRF** and **Sat-NeRF** integrate shadow modeling and transient object filtering to handle multi-temporal data.

### 2. 3D Gaussian Splatting (3DGS)
* **Mechanism**: Models scenes using millions of explicit, tiny 3D Gaussian ellipsoids.
* **Strengths**: Enables significantly faster training and **real-time rendering** (exceeding 100 FPS).
* **Satellite Adaptation**: Frameworks like **EOGS** and **SatGS** account for seasonal color shifts and complex illumination in large-scale Earth observation.

---

## Key Research Areas & Frameworks

| Topic | Description | Representative Frameworks |
| :--- | :--- | :--- |
| **TDOM Generation** | Creating distortion-free "True" flat maps from 3D data. | Ortho-NeRF, Ortho-3DGS, HyGS-TDOM |
| **Large-Scale Urban** | Modeling entire cities using "divide-and-conquer" strategies. | PG-SAG, Block-NeRF, Mega-NeRF |
| **Shadows & Lighting** | Separating building geometry from temporary shadows. | S-NeRF, Sat-NeRF, SatGS, EO-NeRF |
| **Few-Shot Synthesis** | Building 3D scenes from very limited satellite/UAV images. | UP-NeRF, FSGS, DS-NeRF |
| **3D Change Detection** | Tracking construction or environmental updates over time. | Gaussian Difference, C-NeRF |

---

## Comparative Analysis: NeRF vs. 3DGS

| Feature | Neural Radiance Fields (NeRF) | 3D Gaussian Splatting (3DGS) |
| :--- | :--- | :--- |
| **Representation** | Implicit (MLP Weights) | Explicit (3D Ellipsoids) |
| **Training Speed** | Slow (hours to days) | Fast (up to 10x faster) |
| **Rendering** | Computationally heavy/Slow | Real-time (>100 FPS) |
| **Editability** | Difficult ("Black-box") | High (Individual point control) |
| **Quality** | May suffer from blurred edges | Sharper boundaries/Higher PSNR |

---

## Future Directions
Our survey identifies critical areas for future development:
* **Multi-Model Integration**: Combining LiDAR, SAR, and multispectral data with neural rendering.
* **Transient Element Handling**: Better decoupling of moving cars and seasonal vegetation from permanent structures.
* **GIS Compatibility**: Aligning neural models with geodetic reference frames and standard GIS formats for professional mapping.

## Authors
* **Konark Karia** - SEAS, Ahmedabad University
* **Megh Patel** - SEAS, Ahmedabad University
* **Hardi Makwana** - SEAS, Ahmedabad University
