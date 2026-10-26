
# EMMa-DepthPro

Estimate depth maps from EMMa product images using [Depth Pro](https://github.com/apple/ml-depth-pro), a monocular depth estimation model. Predicted depth maps, focal lengths, and fields of view can be used to reconstruct and visualize 3D point clouds.

Dataset access is handled through [EMMa-Wrapper](https://github.com/AltFLanca/EMMa-Wrapper).

## Setup

Install the project dependencies using [uv](https://docs.astral.sh/uv/). From the repository root, run:

```bash
uv sync --locked
```

A prepared EMMa dataset is required. The dataset and Depth Pro model weights are not included in this repository.

## Repository Structure

- `src/test_single.ipynb` - Notebook for testing inference on individual samples and generating 3D point clouds.
- `src/test_inference.ipynb` - Notebook for testing batched depth estimation.

## Run Inference

The current implementation is intended for exploratory inference and visualization. It does not provide a dataset-wide augmentation generation script or HDF5 export pipeline. Depth estimation is explored through the provided Jupyter notebooks.