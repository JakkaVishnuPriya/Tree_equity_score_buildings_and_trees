# Building and Tree Detection Using Deep Learning

## 📌 Project Overview

This project focuses on extracting building footprints and detecting tree canopy regions from satellite imagery using Deep Learning, Computer Vision, and Geospatial Analysis.

The project uses semantic segmentation techniques to identify buildings and tree-covered areas in satellite images. It aims to support urban mapping, environmental monitoring, and **Tree Equity Score (TES) assessment** by providing spatial information about the built environment and urban greenery.

The building detection pipeline uses **U-Net++ with an EfficientNet-B4 encoder**, while the tree canopy detection pipeline applies U-Net++ for pixel-level segmentation.

## 🎯 Objectives

- Detect and extract building footprints from satellite imagery.
- Segment tree canopy regions using deep learning.
- Apply image preprocessing and post-processing techniques to improve segmentation outputs.
- Evaluate segmentation performance using standard metrics.
- Support geospatial analysis for urban environmental assessment.
- Generate useful spatial information for building mapping and tree canopy coverage analysis.

## 🧠 Methodology

### 1. Building Footprint Detection

The building detection pipeline uses **U-Net++ with an EfficientNet-B4 encoder** to perform semantic segmentation of building regions in satellite images.

**Workflow:**
1. Collect and preprocess satellite imagery.
2. Prepare manually labelled building masks and training data.
3. Train the segmentation model using labelled images.
4. Generate pixel-level building predictions.
5. Apply post-processing techniques to refine segmentation masks.
6. Evaluate the model using segmentation metrics.

**Reported evaluation results:**

| Metric | Score |
|---|---:|
| Accuracy | 93.35% |
| Dice Score | 72.81% |
| Intersection over Union (IoU) | 66.01% |
| Loss | 0.42 |

*Note: These are the reported results from the building refinement model. Results may vary depending on the dataset, preprocessing, and evaluation configuration.*

### 2. Tree Canopy Detection

The tree detection pipeline uses **U-Net++ for semantic segmentation** to identify tree canopy regions in satellite imagery.

The model learns to distinguish tree-covered pixels from the surrounding background using labelled training data.

**Workflow:**
1. Prepare satellite images and corresponding tree canopy masks.
2. Preprocess the images and segmentation masks.
3. Train the U-Net++ segmentation model.
4. Generate tree canopy prediction masks.
5. Evaluate the model using segmentation metrics.

The best saved tree segmentation checkpoint achieved the following validation performance:

| Metric | Score |
|---|---:|
| Validation IoU | 0.8326 |
| Validation Dice Score | 0.908 |

*Note: These are validation scores from the saved model checkpoint, not independent test-set results.*

## 🛠️ Technologies Used

- **Programming Language:** Python
- **Deep Learning Framework:** PyTorch
- **Segmentation Architecture:** U-Net++
- **Encoder:** EfficientNet-B4 for building refinement
- **Computer Vision:** OpenCV
- **Geospatial Processing:** Rasterio, GeoPandas, Shapely
- **Numerical Computing:** NumPy
- **Data Analysis:** Pandas
- **Visualization:** Matplotlib
- **Data Sources:** Satellite imagery and labelled segmentation datasets

## 🌳 Applications

- Building footprint extraction
- Tree canopy mapping
- Urban green-space assessment
- Tree Equity Score analysis
- Environmental monitoring
- Satellite image segmentation
- Urban planning and geospatial analysis

## 📊 Evaluation Metrics

The segmentation models can be evaluated using the following metrics:

- **Accuracy:** Measures the proportion of correctly classified pixels.
- **Dice Score:** Measures the overlap between predicted and ground-truth segmentation masks.
- **Intersection over Union (IoU):** Measures the intersection relative to the union of predicted and ground-truth regions.
- **Loss:** Measures the model's training or evaluation error according to the selected loss function.

## 🚀 Future Enhancements

- Integrate building and tree segmentation into a unified geospatial workflow.
- Improve segmentation performance using larger and more diverse labelled datasets.
- Convert building segmentation masks into georeferenced building footprint polygons.
- Estimate tree canopy coverage within defined geographic areas.
- Integrate population and demographic datasets for Tree Equity Score assessment.
- Develop an interactive WebGIS interface for visualizing building footprints and tree canopy predictions.
- Support large-scale satellite imagery processing.

## 👩‍💻 Project Focus

This project demonstrates the application of deep learning, semantic segmentation, computer vision, and geospatial technologies to extract meaningful urban features from satellite imagery.

By combining building footprint detection with tree canopy segmentation, the project provides a foundation for data-driven urban environmental assessment and sustainable city planning.

---

**Keywords:** Building Detection, Tree Canopy Segmentation, Satellite Imagery, Deep Learning, U-Net++, EfficientNet-B4, Semantic Segmentation, Computer Vision, Remote Sensing, Geospatial Analysis, Tree Equity Score.
