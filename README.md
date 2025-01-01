# ComfyUI-Arch-Setup-Nvidia

## Install dependencies
```
yay -Syyu cuda miniconda3
```
add this to your ```.bashrc``` or ```.zshrc```
```
[ -f /opt/miniconda3/etc/profile.d/conda.sh ] && source /opt/miniconda3/etc/profile.d/conda.sh
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
Note: If you get an error export this environment variable ```CRYPTOGRAPHY_OPENSSL_NO_LEGACY=1```
you can add this to your ```.bashrc``` or ```.zshrc```
```
export CRYPTOGRAPHY_OPENSSL_NO_LEGACY=1
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

You can create an alias to put on your ```.bashrc``` or ```.zshrc```
```
alias comfyui='conda activate comfy && python $HOME/ComfyUI/main.py'
```
