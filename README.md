# Tree Detection

The dataset is modified from the [tree classification dataset](https://ytt917251944.github.io/dataset_jekyll/). The dataset is also available on [Kaggle](https://www.kaggle.com/datasets/mcii34/urbantree-subset-public).

On Kaggle, the **tree_detection_dataset** is a subset of the original tree classification dataset, accessible at [this link](https://ytt917251944.github.io/dataset_jekyll/). This dataset includes only the original images, each with a resolution of **1200x1600**. A further refined subset, **Urben Tree Detection.v1i.yolov11**, includes bounding box annotations specifically for object detection. All augmentations and processing were performed using Roboflow.

### Dataset Configuration

The dataset comprises **2,716 images**, divided as follows:
- **Training Set**: 87% (**2,376 images**)
- **Validation Set**: 8% (**227 images**)
- **Test Set**: 5% (**113 images**)

To ensure uniformity in aspect ratio, all images have been resized to **640x640 pixels** using a "fit" resizing approach, which may introduce black edges. Additionally, **auto-orientation** has been applied for consistency.

### Data Preprocessing and Augmentation

Several **augmentation techniques** have been applied to enhance model robustness and generalization. Each training example generates **three augmented outputs**, expanding the diversity of the dataset. The augmentations include:

- **Flip**: Horizontal flipping.
- **Rotation**:
  - **90° rotations**: Clockwise, counterclockwise, and upside-down.
  - **Minor random rotations**: Between -3° and +3° for slight variations.
- **Grayscale**: Applied to 12% of images to simulate different lighting conditions.
- **Blur**: Up to 1.5 pixels to mimic focus variations.
- **Noise**: Added to up to 0.1% of pixels to introduce subtle distortions.

the first model trained on Roboflow can be acccessed [here](https://universe.roboflow.com/treedetection-hn4hr/urben-tree-detection/model/1)

The datasets and training code can be found on [kaggle](https://www.kaggle.com/datasets/mcii34/urbantree-subset-public)
