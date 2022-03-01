Source code and data for the paper:

> Zong-Kai Liu, Li-Hua Zhang, Bang Liu, Zheng-Yuan Zhang, Guang-Can Guo, Dong-Sheng Ding, and Bao-Sen Shi, ***Deep learning enhanced Rydberg multifrequency microwave recognition*** (arXiv: [2202.13617](arxiv.org/abs/2202.13617)).

[![DOI](https://zenodo.org/badge/408725021.svg)](https://zenodo.org/badge/latestdoi/408725021)

# Abstract
Recognition of multifrequency microwave (MW) electric fields is challenging because of the complex interference of multifrequency fields in practical applications. Due to the exaggerated properties of Rydberg atoms, exploration of Rydberg atom-based measurements for multifrequency MW electric fields is promising in MW radar and MW communications. However, Rydberg atoms are sensitive not only to the MW signal but also to noise from atomic collisions and the environment, meaning that solution of the governing Lindblad master equation of light-atom interactions is complicated by the inclusion of noise and high-order terms. Here, we solve these problems by combining Rydberg atoms with deep learning model, demonstrating that this model uses the sensitivity of the Rydberg atoms while also reducing the impact of noise without solving the master equation. As a proof-of-principle demonstration, the deep learning enhanced Rydberg receiver allows direct decoding of the frequency-division multiplexed (FDM) signal without application of multiple band-pass filters and other complex circuits. An FDM phase shift keying signal carrying a QR code with noise is decoded effectively and the information transmission rate is 900 kbps for four bins with accuracy of 99.32%. The new type of sensing technology for multifrequency MW fields reported here is expected to benefit Rydberg-based MW fields sensing and communication.

# Content

- [`notebook`](./notebook). Jupyer notebook and Mathematica notebooks containing code and explanations to reproduce the results of the paper.
- [`data`](./data). Contains the datasets used in the notebooks.


# Requirements

## Hardware Requirements
CPU: Intel core i7-9750H

RAM: 16 GB

GPU: GTX 1650 with 4 GB memory.

## Software Requirements

### OS Requirements
Windows 10

We donot test these codes on different OS.

### CUDA

The CUDA version is 11.4 and driver version is 471.96 (by ```$nvidia-smi```).

### Python Dependencies
The code uses Python 3.6.11 and Mathematica 11.1. The necessary packages are follows:
```
tensorflow-gpu == 2.1.0
keras == 2.3.1
matplotlib == 3.3.4
seaborn == 0.11.1
scikit-learn == 0.22.2
pandas == 1.3.3
numpy == 1.21.2
scipy == 1.4.1
jupyter == 1.0.0
pydot==1.4.2.
```

# Install
The necessary packages can be installed with `conda`. After installing conda and git, run the following codes:

```bash
git clone https://github.com/ZongkaiLiu/Deep-learning-enhanced-Rydberg-multifrequency-microwave-recognition.git
cd Deep-learning-enhanced-Rydberg-multifrequency-microwave-recognition
conda create --name keras3 python==3.7.*
conda activate keras3
pip install tensorflow-gpu==2.1.0
pip install keras==2.3.1
conda install jupyter notebook
pip install matplotlib==3.3.4
pip install seaborn==0.11.1
pip install scikit-learn==0.22.2
pip install --user h5py==2.10.0
```
If you cannot clone this repo, you can also download these codes and datasets via `Code >> Download ZIP` and `cd` into the folder.

After installing conda and creating the environment, you should add conda path into your environment variables.

Install time: about 10 minutes.

# Demo
After installing, the `deep_learning.ipynb` should be opened by Jupyter notebook.  When running the Jupyter notebook please note that **before running each section, the kernel should be restarted (Kernel >> Restart) in case the `%cd` command is wrong**.

Then the results (including loss during training and confusion matrices, etc.) are visualized in the notebook.

The total run time of `deep_learning.ipynb` is about 5 hours.

`deep_learning_with_results.ipynb` contains the same codes but with results. You can save 5 hours by looking over this notebook.

Running `4bins_fitting.nb`, `20bins_fitting.nb`, and `200MHz_fitting.nb` takes about 2 hours.

Any questions about the codes or data are welcomed to the email lzk1997@mail.ustc.edu.cn or dds@ustc.edu.cn.

# License
This project is covered under the **Apache 2.0 License**.
