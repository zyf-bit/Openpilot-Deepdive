# Openpilot-Deepdive
Openpilot-Deepdive的详细部署教程

原项目地址https://github.com/OpenDriveLab/Openpilot-Deepdive

本仓库中的两个txt文件是win系统下指引数据集所需要的，linux系统下需要将_改成|

由于原项目没有预训练模型，因此使用4张NVIDIA GeForce RTX 3090进行训练，详细参数如下，cuda版本12.2![image](https://github.com/Haibara567/Openpilot-Deepdive/assets/94728547/3efc35ff-9c89-4f4a-a4dc-97eeff02ca7c)

conda install pytorch==2.2.0 torchvision==0.17.0 torchaudio==2.2.0 pytorch-cuda=12.1 -c pytorch -c nvidia

使用上个命令仍然提示没有torchvision，再运行 pip install torchvision==0.17.0成功

由于原项目仅使用comma2k19数据集进行训练，因此我们也一样

batch_size设置为4，num_workers设置为2

使用VScode中的ssh extension，然后打开命令行来看tensorboard
