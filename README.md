# U-Net Image Segmentation

A configurable PyTorch implementation of 2D U-Net with dataset transforms, training utilities, and an inference script. The repository includes qualitative nuclei-segmentation examples from the upstream project.

## Task and architecture

Semantic segmentation assigns a class to each pixel. U-Net combines a contracting encoder with an expanding decoder and skip connections that preserve spatial detail. The configurable `UNet2D` exposes network depth and width.

## Repository map

| Path | Purpose |
| --- | --- |
| `unet/` | Model blocks, datasets, and training utilities |
| `train.py` | Training entry point |
| `predict.py` | Prediction entry point for a saved model |
| `kaggle_dsb18/` | Data Science Bowl example material |
| `docs/img/` | Upstream example input and segmentation images |

## Existing upstream example

| Input | Segmentation |
| --- | --- |
| ![Original tissue](docs/img/tissue_original.png) | ![Segmented tissue](docs/img/tissue_segmented.png) |

These images were supplied upstream. No accuracy or Dice score is claimed here; the upstream README warns that its 3D implementation was untested.

## Usage

`train.py` expects paired `images/` and `masks/` directories. For inference, `predict.py` accepts a dataset path, output path, and saved model path. See [the original CLI reference](UPSTREAM_README.md) for complete arguments.

## Source and license

Based on and adapted from [cosmic-cortex/pytorch-UNet](https://github.com/cosmic-cortex/pytorch-UNet). The [original documentation](UPSTREAM_README.md), original code, and [MIT license](LICENSE) are retained. No model was trained or evaluated for this fork.