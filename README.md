# Tomato Leaf Disease Detection Dataset

## Overview

This dataset is prepared for **tomato leaf disease detection using YOLO object detection models**.

The dataset contains tomato leaf images with manually created bounding-box annotations for **9 classes**. The annotations identify visible regions associated with a disease or healthy leaf condition.

The dataset was collected from multiple sources, followed by data cleaning, preprocessing, manual annotation, and dataset organization into training, validation, and testing sets.

## Classes

The dataset contains the following 9 classes:

| ID | Class               |
| -: | ------------------- |
|  0 | Early Blight        |
|  1 | Healthy             |
|  2 | Late Blight         |
|  3 | Leaf Miner          |
|  4 | Leaf Mold           |
|  5 | Tomato Mosaic Virus |
|  6 | Septoria Leaf Spot  |
|  7 | Red Spider Mite     |
|  8 | TYLCV               |

## Dataset Statistics

* **Images:** 13,229
* **Classes:** 9
* **Annotations:** 55,239 disease/leaf regions
* **Annotation type:** Bounding boxes
* **Format:** YOLO
* **Task:** Object Detection

## Dataset Structure

The dataset follows the standard YOLO directory structure:

```text
dataset_yolo/
│
├── images/
│   ├── train/
│   ├── val/
│   └── test/
│
└── labels/
    ├── train/
    ├── val/
    └── test/
```

Dataset configuration:

```yaml
train: images/train
val: images/val
test: images/test

names:
  0: 'Early Blight'
  1: 'Healthy'
  2: 'Late Blight'
  3: 'Leaf Miner'
  4: 'Leaf Mold'
  5: 'Tomato Mosaic Virus'
  6: 'Septoria Leaf Spot'
  7: 'Red Spider Mite'
  8: 'TYLCV'
```

## Annotation Format

Annotations use the standard YOLO format.

Each object is represented by one line:

```text
class_id x_center y_center width height
```

The coordinates are normalized between `0` and `1`.

Example:

```text
0 0.512 0.438 0.321 0.276
```

Here:

* `0` = Early Blight
* `0.512` = normalized bounding-box center X
* `0.438` = normalized bounding-box center Y
* `0.321` = normalized width
* `0.276` = normalized height

## Data Preparation

The general preparation process was:

1. Data collection from multiple sources
2. Data cleaning
3. Image preprocessing
4. Removal of unsuitable or unusable samples
5. Manual annotation
6. Annotation checking
7. Organization into train, validation, and test sets
8. YOLO-format dataset preparation

## Intended Use

This dataset is intended for:

* Tomato disease detection research
* YOLO object detection experiments
* Computer vision projects
* Academic/FYP experimentation
* Evaluation of disease-region detection

The dataset can also be used as a starting point for further research involving tomato disease recognition and agricultural computer vision.

## Important Note

The disease classes can have visually similar symptoms, and some symptoms may vary depending on disease severity, lighting, leaf condition, and image quality.

The annotations were created manually. Therefore, the dataset may contain some unavoidable annotation or class-label ambiguity, particularly between visually similar diseases.

Users should inspect the annotations and evaluate the dataset according to their own requirements before using it for research or production applications.

## Model Training

The dataset can be used with YOLO-compatible object detection frameworks.

Example dataset configuration:

```yaml
path: /kaggle/working/dataset_yolo

train: images/train
val: images/val
test: images/test

names:
  0: 'Early Blight'
  1: 'Healthy'
  2: 'Late Blight'
  3: 'Leaf Miner'
  4: 'Leaf Mold'
  5: 'Tomato Mosaic Virus'
  6: 'Septoria Leaf Spot'
  7: 'Red Spider Mite'
  8: 'TYLCV'
```

## Current Dataset Purpose

This dataset was prepared as part of a **tomato disease detection component of an academic/FYP project**.

The primary objective is to develop a computer vision system capable of locating and identifying visible tomato leaf disease regions.

## Citation

If you use this dataset in your work, please reference the Kaggle dataset page and the original data sources where applicable.
