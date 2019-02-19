# CODRAS: The COnsolidated Diabetic Retinopathy Assessment Set

Codras contains 605 digital fundoscopy images from two data sets – [DIARETDB1](http://www.it.lut.fi/project/imageret/diaretdb1/) (Kauppi et al. (2007), 89 images) and the [Indian Diabetic Retinopathy Database (IDRiD)](https://idrid.grand-challenge.org) (Porwal et al. (2018), 516 images). Each image has been annotated for three objects:

* optic disk

* haemorrhages and microaneurysms

* hard exudates

Annotation was based on the respective native annotation of each data set by a clinician with experience in diabetic retinopathy. Annotations are in the form of bounding boxes, with clusters of smaller instances generally bundled in a larger 'pattern' bounding box. The format of annotations is designed to work with the YOLO recogniser:

```
1 0.6497201492537313 0.277563202247191 0.19076492537313433 0.14009831460674158
|        |                   |                   |                   |
class    |                   |                   |                   |
         centre x            centre y            width               height
```

All location values are scaled to the respective dimension (i.e. `centre x` and `width` are scaled to total image width, `centre y` and `height` are scaled to total image height).

A `.names` file is included to go with the class labels.
