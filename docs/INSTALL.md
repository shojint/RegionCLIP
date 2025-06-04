## Installation

The installation follows [Detectron2](https://github.com/facebookresearch/detectron2/blob/main/INSTALL.md). Here we provide a quickstart guide, and refer to [the solutions from Detectron2](https://github.com/facebookresearch/detectron2/blob/main/INSTALL.md#common-installation-issues) should any issue arise.

### Requirements
- Linux or macOS with Python ≥ 3.6
- PyTorch ≥ 1.6 and [torchvision](https://github.com/pytorch/vision/) that matches the PyTorch installation
- OpenCV is optional for training and inference, yet is needed by our demo and visualization


### Quick Start

```
# environment
conda create -n regionclip python=3.13
source activate regionclip
conda install nvidia/label/cuda-12.8.1::cuda-toolkit
pip3 install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu128

# RegionCLIP
git clone git@github.com:microsoft/RegionCLIP.git
python -m pip install -e RegionCLIP

# other dependencies
pip install opencv-python timm diffdist h5py scikit-learn ftfy
pip install git+https://github.com/lvis-dataset/lvis-api.git
```

To rebuild, use `rm -rf build/ **/*.so` to clean the old build first. You often need to rebuild detectron2 after reinstalling PyTorch.
