# Toward Fast, Flexible, and Robust Low-Light Image Enhancement
![visitors](https://visitor-badge.glitch.me/badge?page_id=vis-opt-group/SCI) 

[[Paper](https://openaccess.thecvf.com/content/CVPR2022/html/Ma_Toward_Fast_Flexible_and_Robust_Low-Light_Image_Enhancement_CVPR_2022_paper.html)] [[Online Demo](https://replicate.com/vis-opt-group/sci)]

<img src="Figs/Firstfig.png" width="900px"/> 
<p style="text-align:justify">Comparison among recent state-of-the-art methods and our method. KinD is a representative paired supervised method.  EnGAN considers the unpaired supervised learning. ZeroDCE [7] and RUAS [16] introduce unsupervised learning. Our method (just contains three convolutions with the size of 3 × 3) also belongs to unsupervised learning. As shown in the zoomed-in regions, these compared methods appear incorrect exposure, color distortion, and insufficient structure to degrade visual quality. In contrast, our result presents a vivid color and sharp outline. Further, we report the computational efficiency (SIZE, FLOPs, and TIME) in (b) and numerical scores for five types of measurement metrics among three tasks including enhancement (PSNR, SSIM, and EME), detection (mAP), and segmentation (mIoU) in (c), it can be easily observed that our method is remarkably superior to others.

## Self-Calibrated Illumination (SCI) Learning Framework
<img src="Figs/Flowchart.png" width="900px"/> 
<p style="text-align:justify">The entire framework of SCI. In the training phase, our SCI is composed of the illumination estimation and self-calibrated module. The self-calibrated module map is added to the original low-light input as the input of the illumination estimation at the next stage. Note that these two modules are respectively shared parameters in the whole training procedure. In the testing phase, we just utilize a single illumination estimation module.</p>

## Requirements
* python3.7
* pytorch==1.8.0
* cuda11.1

## Test steps
* Prepare the data and put it in the specified folder
* Select specific model (difficult.pt medium.pt easy.pt)
* run "test.py"

## Results on Low-light Image Enhancement
<img src="Figs/LLIE_1.png" width="900px"/> 
<img src="Figs/LLIE_2.png" width="900px"/> 
<img src="Figs/LLIE_3.png" width="900px"/> 
<img src="Figs/LLIE_4.png" width="900px"/> 

## Results on High-level Vision Tasks
<img src="Figs/Det_1.png" width="900px"/> 
<img src="Figs/Seg_1.png" width="900px"/> 
<img src="Figs/Seg_2.png" width="900px"/> 

## Citation
```bibtex
@inproceedings{ma2022toward,
  title={Toward Fast, Flexible, and Robust Low-Light Image Enhancement},
  author={Ma, Long and Ma, Tengyu and Liu, Risheng and Fan, Xin and Luo, Zhongxuan},
  booktitle={Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition},
  pages={5637--5646},
  year={2022}
}
```
