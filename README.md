# U-Net, U-Net++ model implementation and comparison
- **using KITTI dataset**

The purpose of the project is to compare the IoU of U-Net, U-Net++ models.  

In addition, U-Net++ will compare two more elements:
1. Compare Up-Sampling 2D() and Conv2Dtranspose() methods of image Up-Sampling

2. Compare binary_crossentropy and bce_dice_loss[custom loss function]

----
해당 git 노트북의 목적은 U-Net과 U-Net++ 각 모델의 IoU 비교입니다.       
추가로, U-Net++은 다음 2가지에 대해서도 비교를 진행합니다.  

1. Upsampling하는 2가지 방법인 UpSampling2D()와 Conv2DTranspose() 비교  

2. keras에서 제공되는 loss인 binary_crossentropy와 custom loss인 bce_dice_loss 비교   





## Semantic Segmentation [U-Net++]
각 모델의 결과는 다음과 같습니다.   

### Conv2DTranspose + bce_dice_loss 
![conv2DTranspose_bce_dice_loss.png](./images/conv2DTranspose_bce_dice_loss.png)

- **index_1 IoU : 0.931261**

<br>

---

### Conv2DTranspose + binary_crossentropy

![conv2DTranspose__binary_crossentropy.png](./images/conv2DTranspose__binary_crossentropy.png)
- **index_1 IoU : 0.764263**

<br>

---

### UpSampling2D + bce_dice_loss
![UpSampling__bce_dice_loss.png](./images/UpSampling__bce_dice_loss.png)


- **index_1 IoU : 0.738070**

<br>

---

### UpSampling2D + binary_crossentropy
![UpSampling__binary_crossentropy.png](./images/UpSampling__binary_crossentropy.png)


- **index_1 IoU : 0.860976**

<br>


---

<br><br>
위의 결과를 표로 나타내면 다음과 같습니다.   

### Nested U-Net 

![U-NetPlus_models.jpg](./images/U-NetPlus_models.jpg)

---


## Semantic Segmentation [U-Net]
![U-Net_Segmentation.png](./images/U-Net_Segmentation.png)


- **index_1 IoU : 0.893522** 

<br>

---

## U-Net vs U-Net++ 
![U-NetPlus_U-Net.jpg](./images/U-NetPlus_U-Net.jpg)


- **U-Net++**의 결과가 더 좋은것을 확인할 수 있습니다.   


---

### References
- **[Nested U-Net author blog](https://sh-tsang.medium.com/review-unet-a-nested-u-net-architecture-biomedical-image-segmentation-57be56859b20)**
