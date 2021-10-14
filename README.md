Source code and data for the paper:

> Zong-Kai Liu, Li-Hua Zhang, Bang Liu, Zheng-Yuan Zhang, Guang-Can Guo, Dong-Sheng Ding, and Bao-Sen Shi, ***Deep learning enhanced Rydberg multifrequency microwave recognition***.


# Abstract
Recognition of multifrequency microwave (MW) electric fields is challenging because of the complex interference of multifrequency fields in practical applications. Due to the exaggerated properties of Rydberg atoms, exploration of Rydberg atom-based measurements for multifrequency MW electric fields is promising in MW radar and MW communications. However, Rydberg atoms are sensitive not only to the MW signal but also to noise from atomic collisions and the environment, meaning that solution of the governing Lindblad master equation of light-atom interactions is complicated by the inclusion of noise and high-order terms. Here, we solve these problems by combining Rydberg atoms with deep learning model, demonstrating that this model uses the sensitivity of the Rydberg atoms while also reducing the impact of noise without solving the master equation. As a proof-of-principle demonstration, the deep learning enhanced Rydberg receiver allows direct decoding of the frequency-division multiplexed (FDM) signal without application of multiple band-pass filters and other complex circuits. An FDM phase shift keying signal carrying a QR code with noise is decoded effectively and the information transmission rate is 900 kbps for four bins with accuracy of 99.32$\%$. The new type of sensing technology for multifrequency MW fields reported here is expected to benefit Rydberg-based MW fields sensing and communication.

# Content

- [`notebook`](./notebook). Jupyer notebooks containing code and explanations to reproduce the results of the paper.
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
The code uses Python 3.6.11.  The necessary packages are written in `environment.yml` file.

# Install
The necessary packages can be installed with `conda`.
To install all the required packages in one go, we include `environment.yml` file.

You can create a new environment and replicate the one used to run these notebooks running the following command in a terminal (from the directory containing `environment.yml`):

```bash
$git clone https://github.com/ZongkaiLiu/Deep-learning-enhanced-Rydberg-multifrequency-microwave-recognition.git
$cd Deep-learning-enhanced-Rydberg-multifrequency-microwave-recognition
$conda env create -f environment.yml
```

# During running
When running the Jupyter notebook please note that before running each section, the kernel should be restart (Kernel >> Restart) in case the `%cd` command is wrong.

# License
This project is covered under the **Apache 2.0 License**.
