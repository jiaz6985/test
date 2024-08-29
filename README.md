# Segmentation 

> **Authors:**
> [Xinsheng Wang](https://).

## :book:Table Of Contents

- [Update](#update)
- [Installation](#installation)
- [Pretrained Models](#pretrained_models)
- [Segmentation Dataset](#segmentation_data)
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

## <a name="segmentation"></a>ℹ️Segmentation Dataset

| Dataset Name | Quark Cloud Disk |
| :---------: | :----------: |
| patient1_train | [download](https://pan.baidu.com/s/1uTAFl13xgGAzrnznAApyng?pwd=xiu3)<br>(pwd: xiu3) |
| patient2_train | [download](https://pan.baidu.com/s/1PhXHAQSTOUX4Gy3MOc2t2Q?pwd=79n9)<br>(pwd: 79n9) |
| patient3_train | [download](https://pan.baidu.com/s/1kvM_SB1VbXjbipLxdzlI3Q?pwd=n7dx)<br>(pwd: n7dx) |
| patient1_test | [download](https://pan.baidu.com/s/1uTAFl13xgGAzrnznAApyng?pwd=xiu3)<br>(pwd: xiu3) |
| patient2_test | [download](https://pan.baidu.com/s/1PhXHAQSTOUX4Gy3MOc2t2Q?pwd=79n9)<br>(pwd: 79n9) |
| patient3_test | [download](https://pan.baidu.com/s/1kvM_SB1VbXjbipLxdzlI3Q?pwd=n7dx)<br>(pwd: n7dx) |
| patient1_label | [download](https://pan.baidu.com/s/1uTAFl13xgGAzrnznAApyng?pwd=xiu3)<br>(pwd: xiu3) |

## <a name="pretrained_models"></a>:dna:Pretrained Models

| Model Name | Description |  Quark Cloud Disk |  
| :---------: | :----------: | :----------: |
| patient1.ckpt | IRControlNet trained on filtered laion2b-en  | [download](https://pan.baidu.com/s/1uTAFl13xgGAzrnznAApyng?pwd=xiu3)<br>(pwd: xiu3) |
| patient2.ckpt | IRControlNet trained on ImageNet-1k | [download](https://pan.baidu.com/s/1PhXHAQSTOUX4Gy3MOc2t2Q?pwd=79n9)<br>(pwd: 79n9) |
| patient3.ckpt | IRControlNet trained on FFHQ | [download](https://pan.baidu.com/s/1kvM_SB1VbXjbipLxdzlI3Q?pwd=n7dx)<br>(pwd: n7dx) |
| classification.pt | SwinIR trained on ImageNet-1k | [download](https://pan.baidu.com/s/176fARg2ySYtDgX2vQOeRbA?pwd=vfif)<br>(pwd: vfif) |

## <a name="Usage"></a>📑:Usage

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

## <a name="Usage"></a>📽️:GUI

  The system is divided into four main sections: classification assessment, image segmentation, precise calculation. 

1.Usage

- First, open an Administrator Command Prompt and use the `cd` command to navigate to the `AMM-Seg/vite` directory of your project. Then, type `npm start` to run the project. This will open a browser and navigate to [http://localhost:3000/free](http://localhost:3000/free).

- Next, open a new command prompt and use the `cd` command to navigate to the `AMM-Seg/src/scripts/` directory. Then, enter `python app.py`. This will start the backend server running locally at `127.0.0.1:5000`.
  
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




  
  
  



