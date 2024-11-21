<h1 align="center">ComfyUI-BiRefNet-lite</h1>

<p align="center">
    <br> <font size=5>English</font> | <a href="README_CN.md">中文</a>
</p>


## 介绍

本仓库将BiRefNet最新模型封装为ComfyUI节点来使用，并支持cpu和gpu分块加载，模型缓存特性。<br>
## 特性
特性1: 支持cpu和gpu分块加载<br>
在开启cuda的情况下，指定cpu_size，可将模型部分加载到cpu上
![slot](./assets/feature1.png)<br>
特性2: 模型缓存<br>
特性3: 多种裁剪方式<br>
支持putalpha, naive, alpha_matting三种裁剪方式
![slot](./assets/feature2.png)<br>
<br>

## News
- Nov 19, 2023: 增加`mask_precision_threshold`参数，控制mask的精度阈值，默认为0.1<br>

## 安装 

#### 方法1:

1. 进入节点目录, `ComfyUI/custom_nodes/`
2. `git clone https://github.com/rubi-du/ComfyUI-BiRefNet-lite.git`
3. `cd ComfyUI-BiRefNet-lite`
4. `pip install -r requirements.txt`
5. 重启ComfyUI

#### 方法2:
直接下载节点源码包，然后解压到custom_nodes目录下，最后重启ComfyUI

#### 方法3：
通过ComfyUI-Manager安装，搜索“ComfyUI-BiRefNet-lite”进行安装

## 使用

示例工作流放置在`ComfyUI-BiRefNet-lite/workflow`中<br/>

加载模型有两种方式可选：一是自动下载并加载远程模型，二是加载本地模型（此时需将`load_local_model`设为true，并将`local_model_path`设置为指向models/birefnet目录下的本地模型路径，例如BiRefNet文件夹）<br/>

![](./assets/9e6bf0f9-67a7-41ea-bc4b-d8352e4fac4a.png)
___

![](./assets/model_path.png)


模型下载地址：<br/>
BiRefNet: https://huggingface.co/ZhengPeng7/BiRefNet/tree/main<br/>
BiRefNet_lite-2K: https://huggingface.co/ZhengPeng7/BiRefNet_lite-2K/tree/main<br/>
BiRefNet-portrait: https://huggingface.co/ZhengPeng7/BiRefNet-portrait/tree/main<br/>
BiRefNet-matting: https://huggingface.co/ZhengPeng7/BiRefNet-matting/tree/main<br/>
RMBG-2.0: https://huggingface.co/briaai/RMBG-2.0/tree/main<br/>

___
工作流workflow.json的使用<br/>

![plot](./assets/demo1.png)

___
工作流video_workflow.json的使用<br/>
[workflow地址](./workflow/video_workflow.json)

## 感谢

感谢BiRefNet仓库的所有作者 [ZhengPeng7/BiRefNet](https://github.com/zhengpeng7/birefnet)

部分代码参考了 [MoonHugo/ComfyUI-BiRefNet-Hugo](https://github.com/MoonHugo/ComfyUI-BiRefNet-Hugo) 感谢！