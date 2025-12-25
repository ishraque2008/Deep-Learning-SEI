# Deep-Learning-SEI

This repository provides a deep learning framework for segmenting Solid-Electrolyte Interphase (SEI) grains and grain boundaries (GBs) in simulated HRTEM images using a hierarchical Transformer-based encoder with a Feature Pyramid Network (FPN) decoder. The approach addresses the challenges of low contrast, and fine-scale features by incorporating strong data augmentations, and custom evaluation metrics such as Matthews Correlation Coefficient (MCC) and Area Match (AM). The pipeline includes configurable training, modular code with PyTorch Lightning, and supports both training and inference on materials-science-inspired datasets.
To generate data, please check python package requirements from SEI-Simulation/gen_data/main.
Similrly to set up package requirements the DL model and train, use DL_model/main. To visualize the data run Visualize/visualize.py. Please make sure the sample annotated images are at correct folder.

1. Data Generation: To generate simulated SEI data:

cd SEI-Simulation/gen_data 

Install the required packages and run main.py to generate image-mask pairs.

2. Training the Deep Learning Model: To train or run inference:

cd DL_model

Install the necessary dependencies (e.g., from requirements.txt) and execute main.py.

4. Visualization:
To visualize model predictions and annotated masks:

cd Visualize
python visualize.py

Make sure your sample images are in the sample/images/ folder and corresponding masks are in sample/annotations/.

For a detailed description of the formalism and derivations used in this project, please refer to the following paper:

I.Z. Borshon, V. Jabbari, T.A. Kingston, R. Shahbazian‐Yassar, V. Yurkiv, Deep Learning Analysis of Solid‐Electrolyte Interphase Microstructures in Lithium‐Ion Batteries, Adv Mater Interfaces (2025). https://doi.org/10.1002/admi.202500558.


<img width="975" height="636" alt="Overview" src="https://github.com/user-attachments/assets/1ea19cc4-ff52-4d8d-b7a8-b43e08ecdcae" />



## Citing

@article{borshon2025deep,\\
  title={Deep Learning Analysis of Solid-Electrolyte Interphase Microstructures in Lithium-Ion Batteries},\\
  author={Borshon, Ishraque Zaman and Jabbari, Vahid and Kingston, Todd A and Shahbazian-Yassar, Reza and Yurkiv, Vitaliy},\\
  journal={Advanced Materials Interfaces},\\
  volume={12},
  number={21},
  pages={e00558},
  year={2025},
  publisher={Wiley Online Library}
}
