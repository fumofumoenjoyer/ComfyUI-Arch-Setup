# ComfyUI-Arch-Setup-Nvidia

## Install dependencies
```
yay -Syyu cuda miniconda3
```
## Clone the ComfyUI repo
```
git clone https://github.com/comfyanonymous/ComfyUI.git
```
## Create a conda evironment
```
conda create --name comfy python=3.10
```
```
conda activate comfy
```

## Install python dependencies (nvidia)
```
pip install torch torchvision torchaudio --extra-index-url https://download.pytorch.org/whl/cu121
```
```
cd ~/ComfyUI
```
```
pip install -r requirements.txt
```
## Done
Now you can do 
```
cd ~/ComfyUI
```
```
python main.py
```
The ComfyUI webUI is on http://127.0.0.1:8188/
