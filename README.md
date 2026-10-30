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

* Ho, J., Jain, A., & Abbeel, P. (2020). Denoising diffusion probabilistic models. Advances in neural information processing systems, 33, 6840-6851.
* Nichol, A. Q., & Dhariwal, P. (2021, July). Improved denoising diffusion probabilistic models. In International conference on machine learning (pp. 8162-8171). PmLR.
* Ronneberger, O., Fischer, P., & Brox, T. (2015, October). U-net: Convolutional networks for biomedical image segmentation. In International Conference on Medical image computing and computer-assisted intervention (pp. 234-241). Cham: Springer international publishing.
* Liu, Z., Luo, P., Wang, X., & Tang, X. (2015). Deep learning face attributes in the wild. In Proceedings of the IEEE international conference on computer vision (pp. 3730-3738).
* Ashish, V. (2017). Attention is all you need. Advances in neural information processing systems.

```

