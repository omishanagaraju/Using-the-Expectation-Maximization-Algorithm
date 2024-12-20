# Color Image Segmentation using EM Algorithm

## Overview
This project implements color image segmentation using the Expectation-Maximization (EM) algorithm. The algorithm divides images into different regions based on color distributions, creating distinct segments or "blobs" of super-pixels.

## Description
The project demonstrates image segmentation on three test images:
- Water coins
- Jump
- Tiger

The EM algorithm is run with varying numbers of segments (2, 3, 4, and 5) to show different levels of segmentation detail.

## Algorithm Implementation
The EM algorithm follows these key steps:

1. **Initialization**
   - Set initial parameters (number of segments, pixel values, mean)

2. **Expectation Step**
   - Predict cluster membership probability for each pixel
   - Based on color distribution parameters

3. **Maximization Step**
   - Update model parameters to maximize pixel color likelihood
   - Improve model fit to data

4. **Iteration**
   - Repeat E and M steps
   - Continue until convergence or maximum iterations (20) reached

5. **Final Segmentation**
   - Assign pixels to highest probability clusters
   - Apply KMeans algorithm for final cluster assignment
   - Update pixel labels to cluster center values
   - Clip and smooth output images

## Applications
The segmentation results can be used in various fields:
- Medical imaging
- Autonomous driving
- Object detection and recognition
- Remote sensing

## Results
The project generates a matrix of output images (3 rows × 4 columns) showing segmentation results for each input image with different numbers of segments. Key observations:

- **Water Coins**: Best results with 2 segments, clearly separating coins from water
- **Jump**: Effective separation of subject, snow, sky, and shadows
- **Tiger**: Most complex image, best results with 5 segments, successfully separating tiger stripes from background

## Dependencies
- Python
- Required libraries (TBA based on implementation details)

## Usage

### Setup
1. Clone the repository:
```bash
git clone https://github.com/omishanagaraju/Using-the-Expectation-Maximization-Algorithm/
cd Using-the-Expectation-Maximization-Algorithm
```

2. Download the required input images:
```bash
mkdir input
cd input
# Download the following images:
# - water_coins.jpg
# - jump.jpg
# - tiger.jpg
```

### Running the Code
1. Open the Jupyter notebook:
```bash
jupyter notebook 'Color Image Segmentation EM.ipynb'
```

2. In the notebook:
   - Make sure the input images are in the `input` directory
   - Run all cells in sequence
   - The segmented images will be saved in the `output` directory
   - The final convergence results will be saved as `convergence_results.png`
