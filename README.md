### 实验一：计算机视觉库的安装

### 一、实验目的

掌握 Anaconda 的安装与基本操作，熟悉 GPU 使用环境的配置及对应版本 PyTorch 的安
装，并完成 OpenCV 的安装与配置
### 二、实验内容
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

2.  conda list pytorch 可以看到已经成功安装，信息如下：<img width="1184" height="550" alt="b89652f89811019342e2bafbd44755b7" src="https://github.com/user-attachments/assets/3eedfe89-eff2-46a2-83cc-78df3c9367a3" />

5、PyTorch GPU加速环境验证
torch.cuda.is_available() 、 torch.backends.cudnn.is_available() 结果进行验证，
信息如下：
验证通过！
### 三、实验结果分析

本次实验完成了计算机视觉实验环境的基本搭建。首先，通过 Anaconda 创建并配置了独立的 Python 虚拟环境，能够正常进入相应环境并进行后续软件安装。随后，在虚拟环境中成功安装 OpenCV，满足后续计算机视觉实验对图像处理库的使用需求。

在 GPU 加速环境配置方面，通过 `nvidia-smi` 对显卡状态进行了查看，并根据对应版本完成 CUDA 和 cuDNN 的配置。之后结合 CUDA 版本安装 PyTorch，并通过 `conda list pytorch` 检查 PyTorch 的安装情况，结果表明 PyTorch 已成功安装。

最后，通过 `torch.cuda.is_available()` 和 `torch.backends.cudnn.is_available()` 对 PyTorch 的 GPU 加速环境进行了验证，验证结果通过，说明当前计算机已经具备使用 GPU 进行深度学习计算的基本条件。

综合实验结果来看，本次实验各项环境配置基本正常，Anaconda、OpenCV、CUDA、cuDNN 和 PyTorch 均能够满足后续计算机视觉实验的使用要求，为后续开展图像处理、深度学习模型训练等实验提供了必要的软件和硬件环境支持。

### 四、实验小结

通过本次实验，我初步掌握了计算机视觉实验环境的搭建方法，进一步熟悉了 Anaconda 及 conda 虚拟环境的基本操作，并完成了 OpenCV、CUDA、cuDNN 和 PyTorch 等相关工具与环境的配置。实验过程中，通过创建独立的 Python 虚拟环境，可以有效管理不同实验所需的软件版本，为后续计算机视觉实验提供了更加稳定、规范的运行环境。

同时，本次实验对 GPU 加速环境进行了配置，并结合 PyTorch 对 CUDA 和 cuDNN 的可用性进行了验证，最终验证通过。通过实际操作，我对 GPU 加速在深度学习模型训练中的作用有了更加直观的认识，也进一步了解了计算机视觉项目从环境配置到程序运行的基本流程。

总体而言，本次实验虽然基础，但为后续计算机视觉相关实验和深度学习模型的学习奠定了良好的环境基础，也提高了我独立配置实验环境、排查安装问题和进行环境验证的能力。
