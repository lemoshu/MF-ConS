# MF-ConS

This repository contains the **PyTorch implementation** of our paper:

> **[Multi-Faceted Consistency Learning with Active Cross-Labeling for Barely-Supervised 3D Medical Image Segmentation]()**  
> *MICCAI, 2024*

---

## 🧠 Introduction

### 📄 Abstract

Achieving accurate 3D medical image segmentation typically requires dense voxel-level annotations, which are costly and time-consuming. To reduce annotation burden, we propose **MF-ConS**, a **Multi-Faceted Consistency Learning** framework designed for a new setting termed **Active Barely-Supervised Learning (Active BSL)**.

MF-ConS builds upon a teacher-student architecture and introduces a **cross-annotation strategy** where only three orthogonal slices (axial, sagittal, and coronal) per scan are labeled. To further optimize labeling efficiency, we integrate an **active learning module (DUS-AL)** that selects the most diverse and uncertain samples.

MF-ConS introduces three complementary consistency constraints:
- **Neighbor-Informed Object Prediction (NIOP)** for enhancing fine-grained contextual understanding,
- **Prototype-driven Consistency** for feature compactness and discriminativeness,
- **Stability Constraint** for robustness under perturbations.

---

## ✅ To-Do List

- [ ] 🔧 Reorganize and clean up the code repository structure  
- [ ] 📂 Add instructions and scripts for each dataset
  - [ ] BraTS 2019 (T2-FLAIR)
  - [ ] Left Atrium (GE-MRI)
  - [ ] Pancreas (NIH-CT)


## 🛠 Requirements

- Python == 3.7  
- PyTorch >= 1.6  
- CUDA toolkit (tested with CUDA 10.2)  
- `scikit-learn`, `scipy`, `numpy`, `SimpleITK`, `matplotlib`

(Refer to `requirements.txt` for a full list.)

---

## 💻 Usage

1. Clone the Repository

```bash
git clone https://github.com/lemoshu/MF-ConS.git
cd MF-ConS
```


2. Data Preparation
Refer to ./data for details


3. Train
```bash
python train_MFConS_{}_3D.py --labeled_num {} --budge {} --gpu 0 --active_type uncer_div
```

5. Test
```bash
python test_3D.py --gpu 0 --exp {}
```


## :books: Citation

If you find this paper useful, please cite as:
```bibtex
@article{wu2025mfcons,
  title={Few Slices Suffice: Multi-Faceted Consistency Learning with Active Cross-Annotation for Barely-supervised 3D Medical Image Segmentation},
  author={Wu, Xinyao and Xu, Zhe and Tong, Raymond Kai-yu},
  journal={MICCAI},
  year={2024}
}
```

