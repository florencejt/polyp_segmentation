
# AMLH Coursework 2022 - RLGJ6

For this coursework I needed to access the GPU on my M1 Mac so I used a nightly build of PyTorch, following these instructions (source: https://www.mrdbourke.com/pytorch-apple-silicon/)

**Zip file structure**
This is the file structure that will let the code run smoothly:
```
RLGJ6-CHME0035
│   README.md
│   requirements.txt    
│   RLGJ6-CHME0035-notebook.ipynb
|   RLGJ6-CHME0035-report.pdf
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

Sorry, I don't have a non-M1 Mac to test that the Conda build works elsewhere.
```
conda create --name RLGJ6-amlh-env python=3.8
conda activate RLGJ6-amlh-env
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
2. **Open the ```RLGJ6-notebook.ipynb``` file in jupyter notebook**
3. **Change the kernel to ```RLGJ6-amlh-env```**

