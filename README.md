### [**ProFiT**](https://www.sciencedirect.com/science/article/)

The official implementation for "**ProFiT: A Prompt-Guided Frequency-Aware Filtering and Template-Enhanced Interaction Framework for Hyperspectral Video Tracking**", ISPRS Journal of Photogrammetry and Remote Sensing (ISPRS), 2025.

--------------------------------------------------------------------------------------

:running:Keep updating:running:: We have released the code and result of ProFiT. (DOING)

--------------------------------------------------------------------------------------
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
- Red --> ProFiT. Blue --> Ground Truth. The Rest --> Compared Arts.
- ![image](/fig/duck.gif)
- ![image](/fig/leaf.gif)
- ![image](/fig/rain.gif)

##  Install
```
git clone https://github.com/YZCU/ProFiT.git
```
## Environment
 > * CUDA 11.8
 > * Python 3.9.18
 > * PyTorch 2.0.0
 > * Torchvision 0.15.0
 > * numpy 1.25.0

--------------------------------------------------------------------------------------
:running:Keep Updating:running:: More detailed tracking results for ProFiT have been released.
| Benchmark (Metrics)            | ProFiT (Pre / Suc)  | Results                                                                   |
| ------------------------------ | ------------------- | ------------------------------------------------------------------------- |
| [HOTC20test](https://www.hsitracking.com/)           |  0.971 / 0.758  | https://github.com/YZCU/ProFiT/tree/main/tracking_results/hotc2020        |
| [HOTC23val_NIR](https://www.hsitracking.com/)        |  0.947 / 0.754  | https://github.com/YZCU/ProFiT/tree/main/tracking_results/hotc2023_nir    |
| [HOTC23val_RedNIR](https://www.hsitracking.com/)     |  0.755 / 0.613  | https://github.com/YZCU/ProFiT/tree/main/tracking_results/hotc2023_rednir |
| [HOTC23val_VIS](https://www.hsitracking.com/)        |  0.915 / 0.720  | https://github.com/YZCU/ProFiT/tree/main/tracking_results/hotc2023_vis    |
| [HOTC24val_NIR](https://www.hsitracking.com/)        |  0.949 / 0.763  | https://github.com/YZCU/ProFiT/tree/main/tracking_results/hotc2024_nir    |
| [HOTC24val_RedNIR](https://www.hsitracking.com/)     |  0.750 / 0.581  | https://github.com/YZCU/ProFiT/tree/main/tracking_results/hotc2024_rednir |
| [HOTC24val_VIS](https://www.hsitracking.com/)        |  0.721 / 0.561  | https://github.com/YZCU/ProFiT/tree/main/tracking_results/hotc2024_vis    |
| [MSSOT](https://www.sciencedirect.com/science/article/pii/S0924271623002551)             |  0.857 / 0.602  | https://github.com/YZCU/ProFiT/tree/main/tracking_results/mssot           |
| [MSVT](https://www.sciencedirect.com/science/article/pii/S0924271621002860)             |  0.967 / 0.754  | https://github.com/YZCU/ProFiT/tree/main/tracking_results/msvt            |

--------------------------------------------------------------------------------------

##  Install
```
git clone https://github.com/YZCU/ProFiT.git
```
## Environment
 > * CUDA 11.8
 > * Python 3.9.18
 > * PyTorch 2.0.0
 > * Torchvision 0.15.0
 > * numpy 1.25.0 
 - Please check the `requirement.txt` for more env details.


## Usage
- Training: Download the RGB/Hyperspectral training/test datasets: [LaSOT](https://cis.temple.edu/lasot/), [GOT-10K](http://got-10k.aitestunion.com/downloads), [COCO](http://cocodataset.org), [HOTC](https://www.hsitracking.com/hot2022/), [MSSOT](https://github.com/Chenlulu1993/SMT), [MSVT](https://github.com/polwork/HOMG), and [TrackingNet](https://tracking-net.org/#downloads).
- Fast Training: Please download the [pre-trained model](https://pan.baidu.com)(code: yzcu) of SpectralTrack and SpectralTrack+'s. Please Put the pre-trained model into <pretrained_models>.
- Run <tracking/0train_SpectralTrack.py> and <tracking/0train_SpectralTrack+.py> to train SpectralTrack. SpectralTrack+--><tracking/0train_SpectralTrack+.py>
- The trained SpectralTrack model will be saved in <output/train/yzcu/yzcu/yzcu_ep0030.pth.tar>. SpectralTrack+--><output/train/yzcu/yzcu+/yzcu_ep0030.pth.tar>
- We have also released the trained [SpectralTrack](https://pan.baidu.com)(code: yzcu) and [SpectralTrack+](https://pan.baidu.com)(code: yzcu) tracking models.
- Testing: Run <tracking/1test_SpectralTrack+.py>. <tracking/1test_SpectralTrack+.py>--><output/results/yzcu/yzcu+>
- For evaluation, please download the evaluation benchmark [Toolkit](http://cvlab.hanyang.ac.kr/tracker_benchmark/) and [vlfeat](http://www.vlfeat.org/index.html) for more precision performance evaluation.
- Refer to [HOTC](https://www.hsitracking.com/hot2022/) for evaluation.
- Evaluation of the SpectralTrack and SpectralTrack+ tracker. Run `\tracker_benchmark_v1.0\perfPlot.m`
- Relevant tracking results are provided in `SpectralTrack and SpectralTrack+\tracking_results\hotc20test`.

:heart:  :heart:

<!---

## Results
- Performance evaluation with hyperspectral arts on the HOTC20’s hyperspectral modality. (a) Precision plot. (b) Success plot.
 ![image](/fig/hotc20.jpg)

- Accuracy-speed trade-off of SOTA hyperspectral arts on the HOTC20 benchmark.
 ![image](/fig/fps.jpg)

-  Subfigures (a) through (f) represent precision plots for NIR23, RedNIR23, VIS23, NIR24, RedNIR24, and VIS24 benchmarks, respectively, while (g) through (l) illustrate corresponding success plots across the same benchmarks.
 ![image](/fig/hotc23-24.jpg)

- Performance evaluation with hyperspectral arts and RGB arts on the MSSOT benchmark. (a) Precision plot. (b) Success plot.
 ![image](/fig/mssot.jpg)

- Performance evaluation with hyperspectral arts and RGB arts on the MSVT benchmark. (a) Precision plot. (b) Success plot. 
 ![image](/fig/msvt.jpg)

- Comprehensive attribute-level and overall success plots of hyperspectral arts and RGB arts on the MSVT benchmark. 
 ![image](/fig/msvt_attr.jpg)

- Visual comparisons, arranged from top to bottom, covering a diverse set of benchmarks: HOTC20 (toy2), VIS23 (cards16), NIR24 (rider14), RedNIR24 (rainystreet12), VIS24 (heartsurgery2), MSSOT (car-16), and MSVT (triple).
 ![image](/fig/vis.jpg)

- Overlap curves and tracking samples of ProFiT are presented in various complex scenarios.
 ![image](/fig/curve.jpg)
-->

:heart:  :heart:

## Contact
If you have any questions or suggestions, feel free to contact me.  
Email: yzchen1006@163.com 

:heart:  :heart: We sincerely appreciate the insightful feedback provided by the editors and reviewers. :heart:  :heart:
