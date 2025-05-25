# ⚙️ ADC
🛠️ This repository provides the official implementation of the paper  
**"Balancing Discrepancy and Consistency: Adversarial Single Domain Generalization in Fault Diagnosis"**.

It includes the network architecture, loss functions, FFT-based data processing, and comparisons for single-domain generalization in intelligent fault diagnosis tasks.
# 🔗 Data link
1. Paderborn University (PU) dataset: [https://mb.uni-paderborn.de/kat/forschung/datacenter/bearing-datacenter/](https://mb.uni-paderborn.de/en/kat/research/kat-datacenter/bearing-datacenter/data-sets-and-download)
2. Huazhong University of Science and Technology (HUST) dataset: https://github.com/CHAOZHAO-1/HUSTbearing-dataset.
3. Beijing University of Technology (BJUT) dataset: https://github.com/Liudd-BJUT/WT-planetary-gearbox-dataset/tree/master
4. Shandong University of Science and Technology(SDUST) dataset: https://github.com/JRWang-SDUST/SDUST-Dataset.git
5. Real Factory Bearing (RFB) dataset: https://drive.google.com/drive/folders/1DHthZwWF6UCn5ukUCBAqJUe1uBwbxXX8?usp=share_link
# ⚙️ Data preprocessing
The raw input data consists of **vibration acceleration signals**. We do not apply any additional preprocessing steps such as denoising or normalization. 

- Each sample is extracted by segmenting the original signal into fixed-length windows.
- A **Fast Fourier Transform (FFT)** is applied to each segment during data loading, implemented in `load_data.py`.

This ensures that the entire pipeline is simple, reproducible, and focused on frequency-domain representations only.

👉 Download the segmented time-domain data here:  
[📥 Click to download time-domain dataset](https://your-download-link.com)
# 🧪 Environment Setup
This project is developed and tested under Python 3.9 with PyTorch ≥ 1.12.

We recommend using `conda` to manage the environment for consistent dependencies.

# 📁 Project Structure
 ADC

├── module/ # Loss functions and modules

├── load_data.py # Data loading and FFT

├── data # Quick-run example data provided

├── Comparison Methods # Code for the relevant comparison method

├── construct_loader.py # Dataloader builder

├── main.py # Training and evaluation

└── README.md
# 🚀 Quick Start

We provide a sample dataset and a ready-to-run script so that users can quickly reproduce the results.

1. **Preparing data**
- Option 1: Use the dataset already included in the `./data/` folder (if you downloaded the full repository ZIP).
- Option 2: Download the data manually from: [📥 External download link](https://your-download-link.com)

2. **Place the dataset in the `./data/` directory** (create this folder if it doesn't exist).

3. **Clone this repository**.
   
4. **Run the** main.py **file to start training and evaluation**.


# 🔬 Comparative Methods

We compare our method with the following state-of-the-art single-domain generalization and fault diagnosis methods:

| Method   | Paper Link |
|----------|------------|
| MEADA    | [Maximum-Entropy Adversarial Data Augmentation for Improved Generalization and Robustness](https://proceedings.neurips.cc/paper/2020/hash/a5bfc9e07964f8dddeb95fc584cd965d-Abstract.html) |
| L2D      | [Learning To Diversify for Single Domain Generalization](https://openaccess.thecvf.com/content/ICCV2021/html/Wang_Learning_To_Diversify_for_Single_Domain_Generalization_ICCV_2021_paper.html)|
| AMINet   | [Adversarial Mutual Information-Guided Single Domain Generalization Network for Intelligent Fault Diagnosis](https://ieeexplore.ieee.org/abstract/document/9774938) |
| MSGACN   | [Multi-scale style generative and adversarial contrastive networks for single domain generalization fault diagnosis](https://www.sciencedirect.com/science/article/pii/S0951832023007937) |
| ACL      | [Single domain generalization method based on anti-causal learning for rotating machinery fault diagnosis](https://www.sciencedirect.com/science/article/pii/S0951832024003247) |
| DEFSDG   | [Domain expansion fusion single-domain generalization framework for mechanical fault diagnosis under unknown working conditions](https://www.sciencedirect.com/science/article/pii/S0952197624015380) |

> ✅ The implementation of all the above comparative methods has been included in this repository under the `Comparison Methods/` directory.


# 📬 Contact

If you have any questions, feel free to open an issue or contact the author.

📮 Contact will be made publicly available after the paper is accepted.
