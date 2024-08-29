# Segmentation 

> **Authors:**
> [Xinsheng Wang](https://).

## :book:Table Of Contents

- [Update](#update)
- [Installation](#installation)
- [Pretrained Models](#pretrained_models)
- [Inference](#inference)
- [Train](#train)

## <a name="update"></a>:new:Update

- **2024.08.30**: This repo is released.

## <a name="installation"></a>:gear:Installation

```shell
# clone this repo
git clone https://github.com/XPixelGroup/DiffBIR.git
cd DiffBIR

# create environment
conda create -n diffbir python=3.10
conda activate diffbir
pip install -r requirements.txt
```
## <a name="pretrained_models"></a>:dna:Pretrained Models

| Model Name | Description | HuggingFace | BaiduNetdisk | OpenXLab |
| :---------: | :----------: | :----------: | :----------: | :----------: |
| v2.pth | IRControlNet trained on filtered laion2b-en  | [download](https://huggingface.co/lxq007/DiffBIR-v2/resolve/main/v2.pth) | [download](https://pan.baidu.com/s/1uTAFl13xgGAzrnznAApyng?pwd=xiu3)<br>(pwd: xiu3) | [download](https://openxlab.org.cn/models/detail/linxinqi/DiffBIR/tree/main) |
| v1_general.pth | IRControlNet trained on ImageNet-1k | [download](https://huggingface.co/lxq007/DiffBIR-v2/resolve/main/v1_general.pth) | [download](https://pan.baidu.com/s/1PhXHAQSTOUX4Gy3MOc2t2Q?pwd=79n9)<br>(pwd: 79n9) | [download](https://openxlab.org.cn/models/detail/linxinqi/DiffBIR/tree/main) |
| v1_face.pth | IRControlNet trained on FFHQ | [download](https://huggingface.co/lxq007/DiffBIR-v2/resolve/main/v1_face.pth) | [download](https://pan.baidu.com/s/1kvM_SB1VbXjbipLxdzlI3Q?pwd=n7dx)<br>(pwd: n7dx) | [download](https://openxlab.org.cn/models/detail/linxinqi/DiffBIR/tree/main) |
| codeformer_swinir.ckpt | SwinIR trained on ImageNet-1k | [download](https://huggingface.co/lxq007/DiffBIR-v2/resolve/main/codeformer_swinir.ckpt) | [download](https://pan.baidu.com/s/176fARg2ySYtDgX2vQOeRbA?pwd=vfif)<br>(pwd: vfif) | [download](https://openxlab.org.cn/models/detail/linxinqi/DiffBIR/tree/main) |


## 1. Introduction

### 1.1. Task Descriptions

<p align="center">
    <img src="http://.png"/> <br />
    <em> 
    Figure 1.[1].
    </em>
</p>

> [1] ****数据集名称*** segmentation dataset, link: https://***********/, accessed: 2024-06-16.

## 2. Proposed Methods

- **Preview:**
  
  *********
  *********
  *********

- **Dataset Preparation:**

    Firstly, you should download the testing/training set  [**数据集链接**](**路径**), 
    and put it into `./Dataset/` repository.
  
- **Download the Pretrained Model:**
  
    **模型名** Pre-trained Models used in our paper (
    [**模型**](**路径**)
    ), 
    and put them into `./所在路径/` repository.

- **Configuring your environment (Prerequisites):**
    
    + Creating a virtual environment in terminal: `conda create -n name python=3.9`.
    
    + Installing necessary packages: `pip install -r requirements.txt`.

### 2.1. Overview

*********
*********
*********

### 2.2. Usage

1. Train

    - In order to run the program, you need to modify some variables in [main.py](https://scripts/main.py "main.py")
    
      cfg['DATA']["data_dir_target"] = input_target_path       #eg."E:/code/data/axis_11"
  
2. Test
    
    - When training is completed, the weights will be saved in `./权重文件路径/`. 
    You can also directly download the pre-trained weights from [权重文件](https://).

    - In order to run the program, you need to modify some variables in [inference.py](https://scripts/inference.py "inference.py")

          data_dir_target = input_path 		                        #eg."E:/code/data/axis_11"     
    
          ckpt_path = model_path 		                                #eg."E:/models/axis_11/model-020000.ckpt"
    
          pred_dir = output_path		                                #eg."E:/scripts/pred_dir"
    
    - All the predictions will be saved in `./分割结果路径`
   
  ## 3. GUI
  
  ### 3.1. Introduction

  The system is divided into four main sections: classification assessment, image segmentation, precise calculation and color change. 

  ### 3.2. Usage

- just run `segmentation_gui.py`.

- The interface is shown below.
  
<p align="center">
    <img src="Classify.png"/> <br />
    <em> 
    Figure 1. Mitochondrial Health Assessment Interface.
    </em>
</p>

<p align="center">
    <img src="Segmentation.png"/> <br />
    <em> 
    Figure 2. Segmentation of 2D Images Interface.
    </em>
</p>

<p align="center">
    <img src="Calculation.png"/> <br />
    <em> 
    Figure 3. Membrane Structure Calculation Interface.
    </em>
</p>

<p align="center">
    <img src="Color.png"/> <br />
    <em> 
    Figure 4. Change Color Interface.
    </em>
</p>

- For detailed GUI guidelines, please refer to the user manual [用户使用手册](https://scripts/inference.py "inference.py")

## 4. Dataset

### 4.1. Training set

The training set consists of mitochondrial cells from myocardial tissue in two regions of one patient.

> - 100 original images sized 800x800 pixels and their corresponding label images.[link](https://)
> - 100 original images sized 800x800 pixels and their corresponding label images.[link](https://)

### 4.2. Testing set

> - 40 original images sized 800x800 pixels and their corresponding label images.[link](https://)

## 5. Results

*********
*********
*********

### 5.1. Download link:

- Segmentation results can be downloaded from this [link](https://)




  
  
  



