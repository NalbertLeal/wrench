<h1 style="text-align:center">
<img style="vertical-align:middle" width="500" height="180" src="./images/wrench_logo.png" />
</h1>

[![made-with-python](https://img.shields.io/badge/Made%20with-Python3-1f425f.svg?color=purple)](https://www.python.org/)
[![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-green.svg)](https://github.com/JieyuZ2/wrench/commits/main)
[![license](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![repo size](https://img.shields.io/github/repo-size/JieyuZ2/wrench.svg)](https://github.com/JieyuZ2/wrench/archive/master.zip)
[![Total lines](https://img.shields.io/tokei/lines/github/JieyuZ2/wrench?color=red)](https://github.com/JieyuZ2/wrench)
![visitors](https://visitor-badge.glitch.me/badge?page_id=JieyuZ2/wrench)
![GitHub stars](https://img.shields.io/github/stars/JieyuZ2/wrench.svg?color=green)
![GitHub forks](https://img.shields.io/github/forks/JieyuZ2/wrench?color=9cf)
[![Arxiv](https://img.shields.io/badge/ArXiv-2109.11377-orange.svg)](https://arxiv.org/abs/2109.11377) 


## **ATTENTION**

**This is a fork of the original wrench repository created to present my personal fix for the installation of the wrench benchmark. The installation using `pip install` always resulted in missing packages, and the `environment.yml` file (that create a conda environment) had many problems with version conflicts among the packages. To fix that, a new `environment.yml` file was created with the correct versions of the required packages (dependencies) to create the conda wrench environment.**

**This repository is entirely based on the original wrench repository; the only modifications are this `README.md` file and the new `environment.yml` file. For information about how to use this benchmark, visit the original repository; there are many useful examples.**

## Creating the environment

1. Make sure to have conda installed.
2. Clone this repository.
3. Navigate to the folder of the cloned repository on your computer.
4. Run the following command to create the conda environment:
    ```bash
    $ conda env create -f environment.yml
    ```
5. Start the environment:
    ```bash
    $ conda activate wrench
    ```
6. Now, inside the repository folder, you can run your Python scripts using the wrench benchmark.

**P.S.: There was no problem with the conda environment creation process using `windows WSL ubuntu`. But, `ubuntu OS` and `pop OS` may require the installation of some libraries used by certain dependencies. That was my experience with the environment creation process.**

**PS. 2: Windows is NOT an option for using wrench. According to reddit users, the package `faiss-gpu` (a dependency of wrench) requires Linux. To use it on Windows, you must use `windows WSL`.**

## Download datasets:

```python
from huggingface_hub import snapshot_download
path = "path to local dir"
snapshot_download(repo_id="jieyuz2/WRENCH", repo_type="dataset", local_dir=path)
```

## 🔧 Citation

**Remember to cite the original benchmark work when you use this repository.**

```
@inproceedings{
zhang2021wrench,
title={{WRENCH}: A Comprehensive Benchmark for Weak Supervision},
author={Jieyu Zhang and Yue Yu and Yinghao Li and Yujing Wang and Yaming Yang and Mao Yang and Alexander Ratner},
booktitle={Thirty-fifth Conference on Neural Information Processing Systems Datasets and Benchmarks Track},
year={2021},
url={https://openreview.net/forum?id=Q9SKS5k8io}
}
```
