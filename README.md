# TM-SCD: Robust Camera-Radar 3D Object Detection for All-Weather Perception

Official PyTorch implementation of the paper: **"TM-SCD: [Robust Radar-Camera 3D Object Detection in bird’s-eye-view for Low-Light and Nighttime Driving]"**.

## ✨ Highlights
This work addresses the challenges of 3D object detection in extreme weather and lighting conditions (e.g., night, dusk, and cluttered backgrounds). 

* **D-CMAF Unit**: A Deformable Cross-Modal Alignment and Fusion unit that utilizes **Deformable Attention** to solve the **Spatial Misalignment** between camera and radar features in the Top-Down View (TDV) domain.
* **HDP-Extractor**: A novel module designed to extract **RCS and geometric structural information** from radar point clouds, compensating for the loss of visual textures in low-light scenarios.
* **Superior Robustness**: Significantly boosts detection performance on the **nuScenes night subset**, achieving a breakthrough from 0.0117 (Camera-only) to **0.3485 (mAP)**.

## 📊 Experimental Results
The following table demonstrates the effectiveness of our D-CMAF strategy compared to baseline fusion methods on the nuScenes night subset:

| Method | Modality | mAP (Night Subset) |
| :--- | :---: | :---: |
| Camera Baseline | C | 0.0117 |
| Concat/Sum Fusion | C + R | ~0.10 |
| **TM-SCD (Ours)** | **C + R** | **0.3485** |

> *Note: Our method handles heterogeneous sensor data more effectively by suppressing radar multipath clutter and leveraging radar depth priors.*



## 🛠️ Repository Structure
- `mmdet3d/models/backbones/`: Implementation of **HDP-Extractor**.
- `mmdet3d/models/necks/`: Implementation of **D-CMAF Unit**.
- `configs/`: Configuration files for reproducing the nuScenes robust analysis results.

## 🔗 Citation
If you find this work useful for your research, please cite:
[Add your BibTeX or paper reference here]
