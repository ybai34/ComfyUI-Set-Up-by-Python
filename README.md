# ComfyUI-Set-Up-by-Python

Welcome to my ComfyUI Set Up by Python repository. This guide offers a simple and easy-to-follow method to set up ComfyUI using Python. It is designed for quick deployment on cloud-based computing platforms, ensuring you can get started swiftly.

## Table of Contents

- [Prerequisites](#prerequisites)
- [Installation](#installation)
  - [Step 1: Download Source Code](#step-1-download-source-code)
  - [Step 2: Install the Model](#step-2-install-the-model)
  - [Step 3: Install Plugins](#step-3-install-plugins)
    - [Basic Plugins](#basic-plugins)
    - [Advanced Plugins](#advanced-plugins)
  - [Step 4: Launch ComfyUI](#step-4-launch-comfyui)
- [Contributing](#contributing)
- [License](#license)

## Prerequisites

Before you begin, ensure you have met the following requirements:
- Python 3.x installed on your machine
- Git installed on your machine
- Internet connection to download dependencies and models

## Installation

### Step 1: Download Source Code

First, clone the ComfyUI repository from GitHub.

```bash
git clone https://github.com/comfyanonymous/ComfyUI
```

Navigate to the ComfyUI directory and set up the virtual environment.

```bash
cd ComfyUI
# Create a virtual environment (uncomment if running for the first time)
# python -m venv venv
# Activate the virtual environment (uncomment if running for the first time)
# source venv/bin/activate
pip install -r requirements.txt
```

### Step 2: Install the Model

Navigate to the ComfyUI directory and download the model.

```bash
cd ComfyUI
wget -P ./models/checkpoints/ http://pai-vision-data-sh.oss-cn-shanghai.aliyuncs.com/aigc-data/sd_models/Counterfeit-V2.5_fp16.safetensors
```

### Step 3: Install Plugins

#### Basic Plugins

Navigate to the `custom_nodes` directory and clone the necessary repositories for basic plugins.

```bash
cd /mnt/workspace/ComfyUI/custom_nodes
git clone https://github.com/ltdrdata/ComfyUI-Manager
git clone https://github.com/AIGODLIKE/AIGODLIKE-COMFYUI-TRANSLATION
git clone https://github.com/AlekPet/ComfyUI_Custom_Nodes_AlekPet
git clone https://github.com/Kosinkadink/ComfyUI-Advanced-ControlNet
git clone https://github.com/Fannovel16/comfyui_controlnet_aux
```

#### Advanced Plugins

##### Face Detailer Plugin

```bash
cd /mnt/workspace/ComfyUI/custom_nodes
git clone https://github.com/ltdrdata/ComfyUI-Impact-Pack.git
```

Install the Face detailer models (upload via OSS recommended).

##### Segment Anything

```bash
cd /mnt/workspace/ComfyUI/custom_nodes
git clone https://github.com/storyicon/comfyui_segment_anything.git
```

##### rembg-comfyui-node

```bash
cd /mnt/workspace/ComfyUI/custom_nodes
git clone https://github.com/Jcd1230/rembg-comfyui-node.git
pip install rembg[gpu]
```

##### Portrait Master Workflow

```bash
cd /mnt/workspace/ComfyUI/custom_nodes
git clone https://github.com/asagi4/comfyui-prompt-control
git clone https://github.com/BlenderNeko/ComfyUI_ADV_CLIP_emb
git clone https://github.com/pythongosssss/ComfyUI-Custom-Scripts.git
```

##### AI Remover

```bash
cd /mnt/workspace/ComfyUI/custom_nodes
git clone https://github.com/hhhzzyang/Comfyui_Lama
```

##### Install the Controlnet Model

Install the Controlnet models (upload via download and OSS recommended).

### Step 4: Launch ComfyUI

Finally, navigate to the ComfyUI directory and launch the application.

```bash
cd /mnt/workspace/ComfyUI/
python main.py
```

## Contributing

Contributions are welcome! Please read the [contributing guidelines](CONTRIBUTING.md) for more information.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
