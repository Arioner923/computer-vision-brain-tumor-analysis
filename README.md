# Computer Vision Brain Tumor Analysis

Academic Computer Vision project focused on identifying, isolating and analyzing three target tumor regions in a provided brain image using classical image-processing techniques.

The project demonstrates a complete processing pipeline including grayscale conversion, manual and automatic thresholding, connected-component labeling, region-area measurement, morphological operations and boundary extraction.

> **Educational use only:** This project is an academic image-processing exercise. It is not a medical diagnostic system and must not be used for clinical diagnosis or medical decision-making.

## Project Objective

The objective is to process the provided brain image and isolate three predefined regions of interest using classical Computer Vision methods.

The workflow includes:

- RGB to grayscale conversion
- Manual thresholding
- Otsu thresholding
- Connected-component labeling
- Tumor-region isolation
- Region-area measurement
- Dilation and erosion
- Morphological opening and closing
- Inner and outer boundary extraction
- Result visualization

## Technologies

- Python
- Jupyter Notebook
- NumPy
- Matplotlib
- SciPy
- scikit-image

## Repository Structure

```text
computer-vision-brain-tumor-analysis/
|
|-- data/
|   `-- brain_tumors.jpg
|
|-- notebooks/
|   `-- computer_vision_brain_tumor_analysis.ipynb
|
|-- results/
|   |-- 01_grayscale_image.png
|   |-- 02_threshold_comparison_50.png
|   |-- 03_threshold_comparison_100.png
|   |-- 04_connected_components.png
|   |-- 05_tumor_regions.png
|   |-- 06_region_areas.png
|   |-- 07_diamond_structuring_element.png
|   |-- 08_image_dilation.png
|   |-- 09_outer_boundaries.png
|   |-- 10_morphological_operations.png
|   `-- 11_final_visualization.png
|
|-- report/
|   |-- report.md
|   `-- computer_vision_brain_tumor_analysis_report.pdf
|
|-- .gitignore
|-- requirements.txt
`-- README.md
```

## Processing Workflow

### 1. Image Preprocessing

The input RGB image is converted to grayscale so that the following operations can work with a single intensity channel.

### 2. Thresholding

Manual thresholding and Otsu's automatic thresholding method are compared. A manual threshold of 50 is initially evaluated, followed by a threshold of 100.

For this specific image, the manual threshold of 100 provides a clearer separation of the three target regions and is therefore used in the following steps.

### 3. Connected-Component Labeling

Connected components in the binary image are assigned individual labels. The three labels corresponding to the target tumor regions are selected and combined into a single binary mask.

### 4. Region Measurement

The three selected regions are labeled again and their areas are measured in pixels. The calculated areas are 531, 592 and 1586 pixels.

### 5. Morphological Processing

A diamond-shaped structuring element is used to demonstrate:

- Dilation
- Erosion
- Opening
- Closing

The inner and outer boundaries of the detected regions are also extracted and visualized.

## Installation and Usage

Clone the repository:

```bash
git clone https://github.com/Arioner923/computer-vision-brain-tumor-analysis.git
cd computer-vision-brain-tumor-analysis
```

Install the required packages:

```bash
pip install -r requirements.txt
```

Run the notebook from the `notebooks` directory so that the relative path to `data/` resolves correctly:

```bash
cd notebooks
jupyter notebook computer_vision_brain_tumor_analysis.ipynb
```

Alternatively, open the repository in VS Code and run the notebook using a Python/Jupyter kernel with the required packages installed.

## Documentation

The detailed project report is available in two formats:

- [`report/report.md`](report/report.md) — GitHub-readable technical report
- [`report/computer_vision_brain_tumor_analysis_report.pdf`](report/computer_vision_brain_tumor_analysis_report.pdf) — formatted PDF version

## Academic Context

This repository is a reorganized and documented version of a university Computer Vision project. The code, results and report have been cleaned up for reproducibility and portfolio presentation while preserving the original project objective and methodology.

## Author

**Vasileios Troupis**  
GitHub: **Arioner923**
