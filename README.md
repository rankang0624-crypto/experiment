实验一：计算机视觉库的安装
一、实验目的
掌握 Anaconda 的安装与基本操作，熟悉 GPU 使用环境的配置及对应版本 PyTorch 的安
装，并完成 OpenCV 的安装与配置
二、实验内容
1、Anaconda的安装及配置
较为简单，不再进行阐述。演示如下：<img width="1483" height="741" alt="289fc189358cf3531d394a4a39b3b04d" src="https://github.com/user-attachments/assets/19bfa0a3-37d2-4375-be5b-1d4ce272a949" />

2、conda的基本操作与OpenCV的安装
1.  conda create -n [env_name] python==[version] 创建虚拟环境并制定python版本。
2.  activate cv 进入创建的虚拟环境， pip install opencv-python 安装OpenCV。演示如
下：<img width="1532" height="742" alt="a5b897776faf64a26480baa988ca0444" src="https://github.com/user-attachments/assets/003eb599-75ec-4806-8904-8e7a96bb7dd1" />

3、GPU加速环境配置
1.  nvidia-smi 显示显卡状态信息，如下：<img width="1472" height="746" alt="3e59337d6b6c5d9e8fa0fb10d8ed8d89" src="https://github.com/user-attachments/assets/180aee38-ab6b-4dbe-ab6b-bc541fb36f1e" />

2. 在NVIDIA官网下载对应版本的CUDA Toolkit及cuDNN并安装，这里不在进行演示。以
下为验证CUDA是否安装成功（cuDNN不能单独运行，后面结合Pytorch验证，这里不做
验证）：
4、PyTorch安装
1. 结合CUDA版本至PyTorch官网选择对应版本进行下载，页面如下：<img width="1772" height="685" alt="866e16af7c1e54e97c03e9f8a6ce9158" src="https://github.com/user-attachments/assets/05780a78-feee-4e21-b640-e2d60f895cfa" />

2.  conda list pytorch 可以看到已经成功安装，信息如下：
5、PyTorch GPU加速环境验证<img width="1184" height="550" alt="b89652f89811019342e2bafbd44755b7" src="https://github.com/user-attachments/assets/f561a985-e030-4136-9f99-e0c724b45d83" />

torch.cuda.is_available() 、 torch.backends.cudnn.is_available() 结果进行验证，
信息如下：
验证通过！
三、实验总结
1. 此次实验较为基础，主要是后续CV实验搭建实验环境。
2. 熟悉了Anaconda虚拟环境管理的基本操作。
3. 结合CUDA与cuDNN配置了GPU加速环境，为深层网络的高效训练奠定了基础
