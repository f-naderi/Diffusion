```markdown
# Face Generation with Diffusion Models (DDPM)

A deep learning project for generating faces using a Denoising Diffusion Probabilistic Model (DDPM) built with TensorFlow 2.21. Trained on the CelebA dataset.

## Features

- DDPM implementation from scratch with U-Net backbone
- Multi-head self-attention for better quality
- Lightweight architecture (~6.5M parameters)
- Automatic best model checkpointing
- Optimized for RTX 4060 Laptop GPU (8GB VRAM)

## Project Structure

Diffusion/
├── archive/                            # CelebA dataset
├── checkpoints/                        # Best model weights
├── final_generated_faces.png           # Grid of 16 generated faces
├── training_history.png                # Loss plot
├── results/                            # Individual face images
├── samples/                            # Training progress samples
├── Diffusion.ipynb                     # Interactive Jupyter notebook
└── requirements.txt                    # Python dependencies

> Note: Some files are excluded from the repository due to their large size

## Installation

```bash
git clone https://github.com/f-naderi/Diffusion.git
cd Diffusion
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

## Model Architecture:
* Type: Denoising Diffusion Probabilistic Model (DDPM)
* Backbone: U-Net with attention
* Diffusion steps: 1000
* Noise schedule: Linear beta
* Loss function: L1 loss
* Optimizer: AdamW with CosineDecay

## Training Details

Dataset: CelebA (202,599 images)
Image size: 64×64
Batch size: 128
Epochs: 20
Initial LR: 1e-3
GPU: RTX 4060 (8GB)

## Results

* Best loss achieved: 0.0829 (epoch 20)
* Improvement from start: 36.2%
* Model size: 6.5M parameters
   
## Requirements

* Python 3.10+
* TensorFlow 
* NumPy
* Matplotlib
* Pillow
* tqdm
* Jupyter Notebook

## References

* Denoising Diffusion Probabilistic Models - Ho et al. (2020)
* Improved Denoising Diffusion Probabilistic Models - Nichol & Dhariwal (2021)
* U-Net: Convolutional Networks for Biomedical Image Segmentation - Ronneberger et al. (2015)
* CelebA Dataset - Liu et al. (2015)
* Attention Is All You Need - Vaswani et al. (2017)

```

