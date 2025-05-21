--------------------------------------------------------------------------------------
### [**ProFiT**](https://www.sciencedirect.com/science/article/)

- The implementation for "**ProFiT: A Prompt-Guided Frequency-Aware Filtering and Template-Enhanced Interaction Framework for Hyperspectral Video Tracking**".
- ISPRS Journal of Photogrammetry and Remote Sensing, 2025.
--------------------------------------------------------------------------------------

:running:Keep updating:running::
- Trained model of [ProFiT](https://drive.google.com/drive/folders/1DACvDnSUr99kkf8lSVH8TtNkCfYiQwok?hl=zh-cn) has been released.
- Training and testing code of [ProFiT](https://github.com/YZCU/ProFiT/blob/main/training%20and%20testing%20codes%20of%20profit.zip) has been released.
- Tracking result of [ProFiT](https://github.com/YZCU/ProFiT/blob/main/rect_result%20of%20profit.zip) has been released.
--------------------------------------------------------------------------------------
| Benchmark | ProFiT (Pre/Suc)|
| ------------------------------ | ------------------- |
| [HOTC20](https://www.hsitracking.com/) |0.971 / 0.758|
| [NIR23](https://www.hsitracking.com/) |0.947 / 0.754|
| [RedNIR23](https://www.hsitracking.com/) |0.755 / 0.613|
| [VIS23](https://www.hsitracking.com/) |0.915 / 0.720|
| [NIR24](https://www.hsitracking.com/) |0.949 / 0.763|
| [RedNIR24](https://www.hsitracking.com/) |0.750 / 0.581|
| [VIS24](https://www.hsitracking.com/) |0.721 / 0.561|
| [MSSOT](https://www.sciencedirect.com/science/article/pii/S0924271623002551) |0.857 / 0.602| 
| [MSVT](https://www.sciencedirect.com/science/article/pii/S0924271621002860) |0.967 / 0.754| 
--------------------------------------------------------------------------------------
- Red --> ProFiT. Blue --> Ground Truth. The Rest --> Compared Arts.
- ![image](/fig/duck.gif)
- ![image](/fig/leaf.gif)
- ![image](/fig/rain.gif)

<!--
- Authors:
[Yuzeng Chen](https://yzcu.github.io/),
[Qiangqiang Yuan](http://qqyuan.users.sgg.whu.edu.cn/),
[Yuqi Tang](https://faculty.csu.edu.cn/yqtang/zh_CN/zdylm/66781/list/index.htm),
Xin Wang,
[Yi Xiao](https://github.com/XY-boy),
Jiang He,
Ziyang Lihe,
Xianyu Jin
--------------------------------------------------------------------------------------
-->
--------------------------------------------------------------------------------------
##  Install
```
git clone https://github.com/YZCU/ProFiT.git
```
--------------------------------------------------------------------------------------
## Environment
 > * CUDA 11.8
 > * Python 3.9.18
 > * PyTorch 2.0.0
 > * Torchvision 0.15.0
 > * numpy 1.25.0 
--------------------------------------------------------------------------------------
## Usage

- Training: Please download the hyperspectral training and testing sets: [HOTC20](https://www.hsitracking.com/hot2022/), [HOTC23](https://www.hsitracking.com/hot2022/), [HOTC24](https://www.hsitracking.com/hot2022/), [MSSOT](https://github.com/Chenlulu1993/SMT), [MSVT](https://github.com/polwork/HOMG). 

- Fast Training: Download the [pre-trained model](https://drive.google.com/drive/folders/1TmeLLUUScQjpFwX1qhvAgmA85E3S6UN0?hl=zh-cn) of ProFiT. Put it into `<pretrained_models>`.
- Run `<tracking/train.py>` to train ProFiT.
- The well-trained ProFiT model is put into `<output/train/yzcu/yzcu-ep150-full-256_shared/yzcu_ep0015.pth.tar>`.
- We have also released the well-trained [ProFiT](https://drive.google.com/drive/folders/1DACvDnSUr99kkf8lSVH8TtNkCfYiQwok?hl=zh-cn) tracking models.
- Testing: Run `<tracking/test.py>` for testing, and results are saved in `<output/results/yzcu/yzcu-ep150-full-256_shared>`.
- Evaluating: Please download the evaluation benchmark [Toolkit](http://cvlab.hanyang.ac.kr/tracker_benchmark/) and [vlfeat](http://www.vlfeat.org/index.html) for more accurate evaluation.
- Refer to the [Hyperspectral Object Tracking Challenge](https://www.hsitracking.com/hot2022/) for detailed evaluations.
- Evaluation of the ProFiT tracker. Run `<tracker_benchmark_v1.0\perfPlot.m>`
--------------------------------------------------------------------------------------
<!--

## Citation
- If you find our work helpful in your research, kindly consider citing it. We appreciate your support！
```
@ARTICLE{11007172,
  author={Chen, Yuzeng and Yuan, Qiangqiang and Xie, Hong and Tang, Yuqi and Xiao, Yi and He, Jiang and Guan, Renxiang and Liu, Xinwang and Zhang, Liangpei},
  journal={IEEE Transactions on Image Processing}, 
  title={Hyperspectral Video Tracking with Spectral-Spatial Fusion and Memory Enhancement}, 
  year={2025},
  volume={},
  number={},
  pages={1-1},
  keywords={Feature extraction;Hyperspectral imaging;Photonic band gap;Foundation models;Visualization;Video tracking;Tracking;Training;Transformers;Imaging;Hyperspectral video tracking;Multi-modal video tracking;Parameter-efficient fine-tuning},
  doi={10.1109/TIP.2025.3569479}}

```
-->

## Contact
- If you have any questions or suggestions, feel free to contact me.  
- Email: yzchen1006@163.com

:heart:  :heart: We sincerely appreciate the insightful feedback provided by Editors and Reviewers. :heart:  :heart:

--------------------------------------------------------------------------------------
