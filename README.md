
# Segmenting polyps in colonoscopy images
By Florence Townend - June 2022

*Description*: Notebook for segmenting polyps in 2D colonoscopy images using a U-Net with modified loss functions. This work was completed as an assessment for Advanced Machine Learning in Healthcare at UCL for the MRes in AI-enabled Healthcare. The data used is Kvasir-SEG, consisting of images from colonoscopy scans and their corresponding segmentation masks. If you want to run this code, the location for this data in the folder structure is indicated below.

For this coursework I needed to access the GPU on my M1 Mac so I used a nightly build of PyTorch, following these instructions (source: https://www.mrdbourke.com/pytorch-apple-silicon/)

**Zip file structure**
This is the file structure that will let the code run smoothly:
```
polyp_segmentation
│   README.md
│   requirements.txt    
│   polyp-segmentation-notebook.ipynb
└───toload
│   │   BCEepoch60.pth
│   │   JSepoch140.pth
|   |   Comboepoch100.pth
|	|	random_search_100_search_output_20epochs_IoULoss.npy
|	|	base_logs.npy
|	|	jaccard_logs.npy
|	|	combo_logs.npy
|	|	base_dict.npy
|	|	jaccard_dict.npy
|	|	combo_dict.npy
└───Kvasir-SEG
|	└───images
|	└───masks
```

1. **Make the environment and install dependencies**

```
conda create --name polypseg python=3.8
conda activate polypseg
```

For an M1 Mac:
```
pip3 install --pre torch torchvision torchaudio --extra-index-url https://download.pytorch.org/whl/nightly/cpu
```
If not an M1 Mac: install torch, torchvision, torchaudio the usual way

Back to normal:
```
conda install nb_conda
pip install -r requirements.txt
pip install ipywidgets
jupyter nbextension enable --py widgetsnbextension
jupyter notebook
```
2. **Open the ```polyp-segmentation-notebook.ipynb``` file in jupyter notebook**
3. **Change the kernel to ```polypseg```**

