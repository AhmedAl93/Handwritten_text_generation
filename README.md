# Text_recognition

### Installation
This repository was run with:
- Python 3.7.3
- Cuda 10.1

Before installing the required packages, set up a virtual environment :
- using venv: python -m venv venv
- using conda: conda create venv

Then activate it:
- using venv: source venv/bin/activate
- using conda: conda activate venv

To install the required packages, run :
- pip install <package_name>==<package_version>

To install PyTorch related packages (torch, torchvision & torchaudio), please refer to the [PyTorch guide](https://pytorch.org/get-started/previous-versions/). Depending on whether conda is used or not, the right command can be found there.

### Procedure
A simple logic was adopted during the development phase, it consists of:
- Generate large, artificial handwritten text dataset.
- Train text recognition model on artificial dataset.
- Once properly trained, finetune the model on the real handwritten text dataset.

The reason behind this logic is the size of real dataset being too small (around 4k images), generating a big artificial dataset was necessary for the model to learn the writing patterns and features of each character.  
Details regarding handwritten text generation and model training can be found in the notebooks Generate_Handwritten_text.ipynb and deep_text_recognition.ipynb respectively.

Model implementation can be found [here](https://github.com/clovaai/deep-text-recognition-benchmark).
