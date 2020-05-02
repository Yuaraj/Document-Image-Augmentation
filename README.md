# Document Image Augmentation
## Introduction
Document Image Augmentation is simple to use tool for performaing Augmentation on Document based Images.<br><br>
This tool provide total 4 types of document Augmentation <br><br>
![Documents Image Type](https://github.com/AyanGadpal/Document-Image-Augmentation/blob/master/Images/AugTypes.jpg)

#### Following are Releasing Soon
1) Add support for Ground Truth 
2) Add Flip and Rotate
3) Add Another Document Specific Augmentation 
4) Modify Color Changer to automatically detect background color

## Quick Start
#### 1. Requirements: numpy & opencv-python
* `pip install numpy`
* `pip install opencv-python`
#### 2. Run ```DocAug.py```; examples:
 * Process a single image: 
    * `python DocAug.py --input_image_filename ../images/image1.jpg`
 * Process all images in a directory : 
    * `python DocAug.py --input_image_dir ../images/ --out_dir ../results/`
#### 3. Python
NOTE : Dialation and Smudge distort the text on the doc, and is useful for object detection task, Do not use this for OCR or text related task <br>
* Dialation
```
AugImage = DocumentAugmention.Dialate(BGRImage)
```
* Smudge
```
AugImage = DocumentAugmention.Smudge(BGRImage)
```
* Color Changer <br>
Color changer will pick random color from 6 distint color and change it with the white background
```
AugImage = DocumentAugmention.changeColor(image)
```

* Brightness Up and Down <br><br>

Increase the Brightness.
```
AugImage = DocumentAugmention.BrightnessUp(BGRImage)
AugImage = DocumentAugmention.BrightnessUp(BGRImage,alpha=50.0)
```
Decrease the Brightness.
```
AugImage = DocumentAugmention.BrightnessDown(BGRImage)
AugImage = DocumentAugmention.BrightnessDown(BGRImage,alpha=50.0)
```
