## Installation

The installation follows [Detectron2](https://github.com/facebookresearch/detectron2/blob/main/INSTALL.md). Here we provide a quickstart guide, and refer to [the solutions from Detectron2](https://github.com/facebookresearch/detectron2/blob/main/INSTALL.md#common-installation-issues) should any issue arise.

### Requirements
- Linux or macOS with Python 3.9
- PyTorch 1.9 and [torchvision](https://github.com/pytorch/vision/) that matches the PyTorch installation
- OpenCV is optional for training and inference, yet is needed by our demo and visualization


### Quick Start

```
# environment
conda create -n regionclip python=3.9
source activate regionclip
conda install nvidia/label/cuda-11.3.0::cuda-toolkit
pip install torch==1.9.1+cu111 torchvision==0.10.1+cu111 torchaudio==0.9.1 -f https://download.pytorch.org/whl/torch_stable.html

# RegionCLIP
git clone git@github.com:microsoft/RegionCLIP.git
python -m pip install -e RegionCLIP

# other dependencies
pip install opencv-python timm diffdist h5py scikit-learn ftfy numpy==1.26.4 setuptools==59.5.0
pip install git+https://github.com/lvis-dataset/lvis-api.git
```

To rebuild, use `rm -rf build/ **/*.so` to clean the old build first. You often need to rebuild detectron2 after reinstalling PyTorch.
