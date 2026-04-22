# Python for Bio Image Analysis

A hands-on workshop notebook introducing Python-based image analysis for biological microscopy data. Written by **Dr Sean Tattan**.

## Overview

This workshop takes you from first principles — working with individual pixel values — through to loading real fluorescence microscopy data, visualising it, and extracting quantitative biological measurements. By the end, you will have segmented nuclei from a multiplexed image and measured fluorescence intensities within them.

## Environment

The notebook uses a Conda environment (`.conda`). Ensure the following packages are installed:

```
numpy
scikit-image
matplotlib
imageio
pandas
```

## Workshop Structure

### 1. Getting Started with Image Data
Introduces Python variables, arithmetic, and the 8-bit pixel value scale (0–255). Covers brightness scaling and normalisation.

### 2. Creating 2D Arrays of Pixels
Builds a checkerboard pattern using NumPy arrays, visualises it with Matplotlib, and demonstrates array-level mathematical operations such as image inversion. Introduces writing reusable functions.

### 3. Displaying Single-Channel Biological Images
Loads a real 16-bit fluorescence image, applies a custom black-to-red colormap, analyses pixel intensity distributions via histogram, and uses percentile-based contrast stretching to improve visualisation without altering raw data.

### 4. Displaying Multiplex Biological Images
Extends to multi-channel `.tif` files, plots individual channels side by side, and creates a merged RGB display image by normalising and colour-mapping each channel.

### 5. Segmenting Images
Covers nucleus segmentation using Otsu's method, morphological post-processing (hole filling and small object removal), and quantitative measurement of transcription factor fluorescence intensity within segmented nuclei using `regionprops_table`.

## Key Concepts

- **8-bit and 16-bit pixel values** and what they represent in fluorescence microscopy
- **NumPy arrays** as image representations
- **Custom colourmaps** for single-channel fluorescence display
- **Contrast stretching** using percentile clipping
- **Binary masking and thresholding** (manual and Otsu)
- **Morphological operations**: hole filling, small object removal
- **Labelling and region properties** for quantitative measurement

## Challenges

Each section includes short exercises marked in bold, such as computing pixel contrast, applying a custom function, and changing channel colour mappings.

## Next Steps

- **Watershed segmentation** to separate touching nuclei: [scikit-image watershed example](https://scikit-image.org/docs/0.25.x/auto_examples/segmentation/plot_watershed.html)
- Batch processing across multiple images
- Statistical comparison of measurements across conditions
