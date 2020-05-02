# Document Image Augmentation
## Introduction
Document Image Augmentation is simple to use tool for performaing Augmentation on Document based Images.<br><br>
This tool provide total 4 types of document Augmentation <br><br>
![Documents Image Type](https://github.com/AyanGadpal/Document-Image-Augmentation/blob/master/Images/AugTypes.jpg)

Following are Releasing Soon
1) Add support for Ground Truth 
2) Add Flip and Rotate
3) Add Another Document Specific Augmentation 
4) Modify Color Changer to automatically detect background color

## Quick Start

## API
#### 1. Dialation and Smduge
NOTE : Dialation and Smudge distort the text on the doc, and is useful for object detection task, Do not use this for OCR or text related task<br>
Dialation
```
AugImage = DocumentAugmention.Dialate(BGRImage)
```
Smudge
```
AugImage = DocumentAugmention.Smudge(BGRImage)
```
#### 2. Color Changer
Color changer will pick random color from 6 distint color and change it with the white background
```
AugImage = DocumentAugmention.changeColor(image)
```

#### 3. Brightness Up and Down
Increase the Brightness. 
```
AugImage = DocumentAugmention.BrightnessUp(BGRImage)
```
You can also specify the amount of Brightness to increase with
```
AugImage = DocumentAugmention.BrightnessUp(BGRImage,alpha=50.0)
```
Decrease the Brightness. 
```
AugImage = DocumentAugmention.BrightnessDown(BGRImage)
```
You can also specify the amount of Brightness to increase with
```
AugImage = DocumentAugmention.BrightnessDown(BGRImage,alpha=50.0)

