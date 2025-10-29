# OSLM Dataset

## Overview

The OSLM  Dataset is a comprehensive collection of SAR (Synthetic Aperture Radar) imagery designed for oil spill detection and segmentation tasks. The dataset integrates multi-source satellite data from Sentinel-1 and GF-3 missions, providing diverse polarimetric configurations to support robust model training and evaluation.
In addition, our data set is too large for you to download directly, we provide you with the following download method.
You can download the dataset from https://pan.quark.cn/s/080b9e9f256c

## Dataset Statistics

| Source | Slices | Resolution | Input Features | 
|--------|--------|------------|----------------|
| **Sentinel-1** | 28,984 | 256×256 | VV | 
| **GF-3** | 2,264 | 256×256 | VV & HH |
| **Simulated CP** | 2,264 | 256×256 | RH & RV |
| **Total** | **33,512** | - | - | 


## Key Features

### 1. Balanced Class Distribution
To mitigate sample imbalance, non-oil spill slices were strategically excluded during dataset construction, optimizing the class distribution within the training data and improving model performance on oil spill detection tasks.

### 2. Multi-Source Integration
- **Sentinel-1 C-band SAR**: Provides extensive coverage with single polarization (VV)
- **GF-3 C-band SAR**: Offers dual-polarization data (VV & HH) for enhanced feature extraction
- **Simulated Compact Polarimetry**: Includes RH & RV channels for advanced polarimetric analysis

### 3. Standardized Format
- All slices are uniformly sized at **256×256 pixels**
- Consistent labeling: Oil spill pixels = 1, Non-oil spill pixels = 0
- TIFF format for easy integration with deep learning frameworks



## Data Format

### Images
- **Format**: .tif/.tiff
- **Size**: 256×256 pixels
- **Channels**: 
  - Sentinel-1: 1 channel (VV)
  - GF-3: 2 channels (VV, HH)
  - Simulated CP: 2 channels (RH, RV)

### Masks
- **Format**: .tif/.tiff
- **Size**: 256×256 pixels
- **Values**: 
  - `1` = Oil spill pixel
  - `0` = Non-oil spill pixel


## Citation



## Acknowledgments

- Sentinel-1 data courtesy of the European Space Agency
- GF-3 data courtesy of the ChinaCentre for Resources Satellite Data and Application

---

**Note**: This dataset is intended for research and educational purposes only.
