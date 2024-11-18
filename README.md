<h1 align="center">ComfyUI-BiRefNet-lite</h1>  
  
<p align="center">  
    <br> <font size=5>English | <a href="README_CN.md">中文</a></font>  
</p>  
  
## Introduction  
  
This repository packages the latest BiRefNet model as a ComfyUI node for use, supporting chunked loading on both CPU and GPU, as well as model caching features.<br>  
  
## Features  
Feature 1: Supports chunked loading on CPU and GPU<br>  
When CUDA is enabled, specify the `cpu_size` to load part of the model onto the CPU.  
![slot](./assets/feature1.png)<br>  
Feature 2: Model Caching<br>  
Feature 3: Multiple Cropping Methods<br>  
Supports putalpha, naive, and alpha_matting cropping methods.  
![slot](./assets/feature2.png)<br>  
<br>  
  
## Installation   
  
#### Method 1:  
  
1. Navigate to the node directory, `ComfyUI/custom_nodes/`  
2. `git clone https://github.com/rubi-du/ComfyUI-BiRefNet-lite.git`  
3. `cd ComfyUI-BiRefNet-lite`  
4. `pip install -r requirements.txt`  
5. Restart ComfyUI  
  
#### Method 2:  
Directly download the node source code package, unzip it into the `custom_nodes` directory, and then restart ComfyUI.  
  
#### Method 3:  
Install via ComfyUI-Manager by searching for "ComfyUI-BiRefNet-lite".  
  
## Usage  
  
Example workflows are placed in `ComfyUI-BiRefNet-lite/workflow`.<br/>  
  
There are two ways to load models: one is to automatically download and load a remote model, and the other is to load a local model. To load a local model, set `load_local_model` to true and `local_model_path` to the location of the local model, e.g., `H:\ZhengPeng7\BiRefNet`.<br/>  
  
![](./assets/9e6bf0f9-67a7-41ea-bc4b-d8352e4fac4a.png)  
___  
  
![](./assets/model_path.png)  
  
Model download links:<br/>  
BiRefNet: https://huggingface.co/ZhengPeng7/BiRefNet/tree/main<br/>  
BiRefNet_lite-2K: https://huggingface.co/ZhengPeng7/BiRefNet_lite-2K/tree/main<br/>  
BiRefNet-portrait: https://huggingface.co/ZhengPeng7/BiRefNet-portrait/tree/main<br/>  
BiRefNet-matting: https://huggingface.co/ZhengPeng7/BiRefNet-matting/tree/main<br/>  
RMBG-2.0: https://huggingface.co/briaai/RMBG-2.0/tree/main<br/>  
  
___  
Usage of workflow.json<br/>  
  
![plot](./assets/demo1.png)  
  
___  
Usage of video_workflow.json<br/>  
[Workflow Address](./workflow/video_workflow.json)  
  
## Acknowledgments  
  
Thanks to all the authors of the BiRefNet repository [ZhengPeng7/BiRefNet](https://github.com/zhengpeng7/birefnet).  
  
Some code was referenced from [MoonHugo/ComfyUI-BiRefNet-Hugo](https://github.com/MoonHugo/ComfyUI-BiRefNet-Hugo). Thank you!