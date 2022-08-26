## _Rotatated airplane Detector based on EfficientDet_   

This **rotation airplane detector** is implemented and modified based on [pytorch implementing EfficientDet(horizontal)](https://github.com/zylo117/Yet-Another-EfficientDet-Pytorch) and you can find original paper [here](https://arxiv.org/abs/1911.09070 "EfficientDet").

## _Experiment_

  Prepare airplane dataset for Task1-Detection with oriented bounding boxes [DOTA dataset](https://captain-whu.github.io/DOTA/)

  
## **evaluation metrics**  

|coefficient|Input Size|mAP(iou=.5)|
|:---------:|:--------:|:---------:|
|D2         |768 x 768 |0.574      |

- loss curve

- Totall loss =  regression loss + clasification loss
 
  ![](imgs/loss-curve.PNG)

### Outputs for rotated airplane detector
---

- Correct detection for all airplanes 
 
   ![](https://github.com/jobe1366/Rotated-airplane-detection/blob/main/imgs/outputs%20of%20detector.PNG)
      
- Detection of airplanes along with some error in detection
 
   ![](https://github.com/jobe1366/Rotated-airplane-detection/blob/main/imgs/errors%20in%20detection.PNG)
