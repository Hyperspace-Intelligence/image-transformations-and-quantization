# Image Transformations and Quantization

A collection of classical image-processing operations: image loading, blur and custom convolution kernels, rotation and cropping, grayscale conversion, intensity quantization, and error-diffusion dithering.

**Status: source implementations included.** Notebooks may need local input data and configuration to run.

## What this covers

- Spatial filtering and 2-D convolution
- Geometric transformations and cropping
- Weighted-average grayscale, desaturation and channel decomposition
- Intensity quantization, Floyd–Steinberg and Burkes error diffusion

## Processing pipeline

~~~mermaid
flowchart LR
    A[Input image] --> B[Spatial and geometric transforms]
    B --> C[Grayscale conversion]
    C --> D[Intensity quantization]
    D --> E[Error diffusion]
    E --> F[Display and compare]
~~~

## Technical explanation

For a colour image, one common luminance approximation is **Y = 0.299R + 0.587G + 0.114B**. Quantization maps a continuous or 8-bit intensity to a smaller discrete set of levels.

## Contents

- `notebooks/image-transformations.ipynb` — from `week01_intro/lab01.ipynb`
- `notebooks/grayscale-and-dithering.ipynb` — from `week02_fundamental_steps/lab02.ipynb`

## Getting started

Use Python 3.10+ in a virtual environment:

~~~bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
jupyter lab
~~~

On Windows, activate with `.venv\Scripts\activate` instead. Install `jupyterlab` if it is not installed already. Open a notebook under `notebooks/`. Dataset/model paths in the original examples may need updating.

## Important limitations

The source notebooks use local demonstration images. Supply your own images and adapt file paths before running. Saved image outputs have been cleared.

Input assets, lecture handouts, PDFs, trained models, cached results and third-party datasets have intentionally not been republished. Notebook code and explanatory cells are retained, while saved cell outputs are removed. No performance claims or additional experiments have been invented.

## Provenance

Adapted from the publicly available [ComputerVision source collection](https://github.com/dbxdrgsl/ComputerVision). Source-to-destination file mappings appear above. Each repository is organized by technical subject rather than course numbering.
