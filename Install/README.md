# Installing Stable Diffusion 

## Locally on Linux

### Step 1: Install Python

    python --version

    python3 --version

If it needs to be downloaded

    sudo apt-get update

    yes | sudo apt-get install python3

Recommened 3.8 but 3.10 also seems fine

### Step 2: Install Miniconda

Check to see if pre-installed

    conda --version

If not to install with 3.8+

    wget https://repo.anaconda.com/miniconda/Miniconda3-py38_4.12.0-Linux-x86_64.sh

    bash Miniconda3-py38_4.12.0-Linux-x86_64.sh

If installed then need to close and reopen the shell to run conda command

### Step 3: Clone the Stable Diffusion Repository

    git clone https://github.com/CompVis/stable-diffusion.git

    cd stable-diffusion/

If need to install git

    sudo apt install git

### Step 4: Create Conda Environment

    conda env create -f environment.yaml

    conda activate ldm

### Step 5: Download Stable Diffusion Weights

    curl https://f004.backblazeb2.com/file/aai-blog-files/sd-v1-4.ckpt > sd-v1-4.ckpt

### Step 6: How to Generate Images with Stable Diffusion (GPU)

    python scripts/txt2img.py --prompt "YOUR-PROMPT-HERE" --plms --ckpt sd-v1-4.ckpt --skip_grid --n_samples 1

