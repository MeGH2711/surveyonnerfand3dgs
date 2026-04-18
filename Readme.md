# Survey on NeRF and 3DGS in Satellite Remote Sensing

## Overview
[cite_start]This repository contains research and documentation related to our survey on **Neural Radiance Fields (NeRF)** and **3D Gaussian Splatting (3DGS)** as applied to satellite remote sensing[cite: 1, 2]. [cite_start]As modern satellites capture vast amounts of data, the field is shifting from flat 2D representations to immersive, high-fidelity **3D digital twins** of urban environments and landscapes[cite: 27, 28, 29].

[cite_start]Our survey explores how these two modern techniques overcome the limitations of traditional photogrammetry—such as shifting shadows, atmospheric changes, and massive dataset sizes—to revolutionize 3D reconstruction from space[cite: 11, 12, 17].

---

## Core Technologies

### 1. Neural Radiance Fields (NeRF)
* [cite_start]**Mechanism**: Uses a deep neural network (typically a Multilayer Perceptron) to represent a scene implicitly as a continuous 5D function[cite: 37, 180].
* [cite_start]**Strengths**: Excellent at handling complex reflections, translucency, and lighting changes[cite: 15, 188].
* [cite_start]**Satellite Adaptation**: Models like **S-NeRF** and **Sat-NeRF** integrate shadow modeling and transient object filtering to handle multi-temporal data[cite: 40].

### 2. 3D Gaussian Splatting (3DGS)
* [cite_start]**Mechanism**: Models scenes using millions of explicit, tiny 3D Gaussian ellipsoids[cite: 16, 44].
* [cite_start]**Strengths**: Enables significantly faster training and **real-time rendering** (exceeding 100 FPS)[cite: 45, 223].
* [cite_start]**Satellite Adaptation**: Frameworks like **EOGS** and **SatGS** account for seasonal color shifts and complex illumination in large-scale Earth observation[cite: 48].

---

## Key Research Areas & Frameworks

| Topic | Description | Representative Frameworks |
| :--- | :--- | :--- |
| **TDOM Generation** | [cite_start]Creating distortion-free "True" flat maps from 3D data[cite: 19, 80]. | [cite_start]Ortho-NeRF, Ortho-3DGS, HyGS-TDOM [cite: 80] |
| **Large-Scale Urban** | [cite_start]Modeling entire cities using "divide-and-conquer" strategies[cite: 20, 80]. | [cite_start]PG-SAG, Block-NeRF, Mega-NeRF [cite: 80, 269] |
| **Shadows & Lighting** | [cite_start]Separating building geometry from temporary shadows[cite: 21, 80]. | [cite_start]S-NeRF, Sat-NeRF, SatGS, EO-NeRF [cite: 80] |
| **Few-Shot Synthesis** | [cite_start]Building 3D scenes from very limited satellite/UAV images[cite: 22, 86]. | [cite_start]UP-NeRF, FSGS, DS-NeRF [cite: 86] |
| **3D Change Detection** | [cite_start]Tracking construction or environmental updates over time[cite: 23, 86]. | [cite_start]Gaussian Difference, C-NeRF [cite: 86] |

---

## Comparative Analysis: NeRF vs. 3DGS

| Feature | Neural Radiance Fields (NeRF) | 3D Gaussian Splatting (3DGS) |
| :--- | :--- | :--- |
| **Representation** | [cite_start]Implicit (MLP Weights) [cite: 178, 311] | [cite_start]Explicit (3D Ellipsoids) [cite: 314] |
| **Training Speed** | [cite_start]Slow (hours to days) [cite: 42, 312] | [cite_start]Fast (up to 10x faster) [cite: 45, 316] |
| **Rendering** | [cite_start]Computationally heavy/Slow [cite: 42, 203] | [cite_start]Real-time (>100 FPS) [cite: 45, 318] |
| **Editability** | [cite_start]Difficult ("Black-box") [cite: 329, 330] | [cite_start]High (Individual point control) [cite: 332, 333] |
| **Quality** | [cite_start]May suffer from blurred edges [cite: 323] | [cite_start]Sharper boundaries/Higher PSNR [cite: 321, 322] |

---

## Future Directions
[cite_start]Our survey identifies critical areas for future development[cite: 335]:
* [cite_start]**Multi-Model Integration**: Combining LiDAR, SAR, and multispectral data with neural rendering[cite: 342, 344].
* [cite_start]**Transient Element Handling**: Better decoupling of moving cars and seasonal vegetation from permanent structures[cite: 351, 359].
* [cite_start]**GIS Compatibility**: Aligning neural models with geodetic reference frames and standard GIS formats for professional mapping[cite: 365, 367, 375].

## Authors
* [cite_start]**Konark Karia** - SEAS, Ahmedabad University [cite: 3, 4]
* [cite_start]**Megh Patel** - SEAS, Ahmedabad University [cite: 6, 7]
* [cite_start]**Hardi Makwana** - SEAS, Ahmedabad University [cite: 8, 9]
