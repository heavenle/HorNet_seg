# HorNet_seg

该代码是已经调通的HorNet模型，用于0.5m遥感建筑物语义分割任务。对于源码基本没啥变化，主要用于自用、以及给各位进行自定义训练作为一个参考。

源码请参考：<br>
[https://github.com/raoyongming/HorNet](https://github.com/raoyongming/HorNet)

个人博客对于HorNet的讲解：<br>
[Segmentation：HorNet 学习总结](https://blog.csdn.net/weixin_43610114/article/details/128145243)

---

- 其中有3个是配置好可以本地运行的训练脚本：<br>
1. train_guowangtong512.py
2. train_bigdata512_large_build_hornet.py
3. train_bigdata512_base_build_hornet.py

- 其中有2个是配置好可以本地运行的预测脚本。该脚本可以生成shp和单波段tif图像：<br>
1. predict_120bigdata_build_512_large.py
2. predict_guowangtong_build_512.py

- 自定义数据的配置文件，我的数据都是基于VOC格式：<br>
1. /config/__base__/datasets/guowangtong512.py

- 自定义网络结果配置文件:<br>
1. /config/hornet/upernet_hornet_large_gf_512_160k_guowangtong.py
2. /config/hornet/upernet_hornet_large_gf_512_160k_bigdata_build.py

## Linux运行环境
package|version
---|---
addict|                        2.4.0
certifi|                       2022.9.24
charset-normalizer|            2.1.1
contourpy|                     1.0.5
cycler|                        0.11.0
flatbuffers|                   22.12.6
fonttools|                     4.37.4
GDAL|                         3.5.2
idna|                          3.4
imageio|                       2.22.2
kiwisolver|                    1.4.4
matplotlib|                    3.6.1
mmcv-full|                     1.4.7
mmdet|                         2.22.0
mmsegmentation|                0.20.2
MultiScaleDeformableAttention| 1.0
networkx|                      2.8.7
numpy|                         1.23.4
onnxruntime-gpu|               1.8.0
opencv-python|                 4.6.0.66
packaging|                     21.3
Pillow|                        9.2.0
pip|                           22.2.2
prettytable|                   3.4.1
protobuf|                      4.21.11
pycocotools|                   2.0.5
pyparsing|                     3.0.9
python-dateutil|               2.8.2
PyWavelets|                    1.4.1
PyYAML|                        6.0
requests|                      2.28.1
scikit-image|                  0.19.3
scipy|                         1.9.2
setuptools|                    65.4.1
six|                           1.16.0
terminaltables|                3.1.10
tifffile|                      2022.10.10
timm|                          0.4.12
torch|                         1.11.0+cu113
torchaudio|                    0.11.0+cu113
torchvision|                   0.12.0+cu113
typing_extensions|             4.4.0
urllib3|                       1.26.12
wcwidth|                       0.2.5
wheel|                         0.37.1
yapf|                          0.32.0

## 使用步骤
1. 修改数据配置文件。
> 例如：/config/__base__/datasets/guowangtong512.py

2. 修改类别配置文件。
> 例如：/mmseg/datasets/build_voc.py

3. 修改训练网络配置文件。
> 例如：/config/hornet/upernet_hornet_large_gf_512_160k_guowangtong.py

4. 修改本地训练脚本
> 例如：./train_guowangtong512.py

5. 修改本地测试脚本（遥感）
> 例如：./predict_120bigdata_build_512_large.py

## 预训练模型

未上传

## 已经训练好的权重

未上传
