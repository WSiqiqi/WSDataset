# WSDataset (Sample)

This repository contains **sample data** for whale detection from satellite imagery in YOLO format.

> **Important Note**: This repository only contains sample data for demonstration and learning purposes.

## Dataset Source

This sample data is derived from the following paper:

**Cubaynes, H.C., Fretwell, P.T.** "Whales from space dataset, an annotated satellite image dataset of whales for training machine learning models." *Scientific Data* **9**, 245 (2022). https://doi.org/10.1038/s41597-022-01377-4

Original Dataset Information:
- **Species Coverage**: Humpback whale, Fin whale, Gray whale, Southern right whale
- **Satellite Sources**: WorldView-3, WorldView-2, GeoEye-1, Quickbird-2
- **Original License**: CC BY 4.0

## Dataset Structure

```
WS/
├── images/
│   ├── train/      # Training samples (23 images)
│   ├── val/        # Validation samples (3 images)
│   └── test/       # Test samples (6 images)
└── labels/
    ├── train/      # Training annotations (23 files)
    ├── val/        # Validation annotations (3 files)
    └── test/       # Test annotations (6 files)
```

## Sample Data Statistics

| Subset | Images | Annotation Files |
|--------|--------|------------------|
| Train samples | 23 | 23 |
| Validation samples | 3 | 3 |
| Test samples | 6 | 6 |
| **Total** | **32** | **32** |

## File Format

- **Image Format**: PNG
- **Annotation Format**: TXT (YOLO format)
- **Coordinate Format**: Normalized bounding boxes (class x_center y_center width height)

## Sample Files

Sample files are located in:
- `images/train/` - Training sample images
- `images/val/` - Validation sample images
- `images/test/` - Test sample images
- `labels/` - Corresponding YOLO format annotation files

## Usage

### YOLO Format Training

This sample data can be used to familiarize yourself with the YOLO model training workflow:

```yaml
# data.yaml configuration example
train: ./images/train
val: ./images/val
test: ./images/test

nc: 1  # Number of classes
names: ['whale']  # Class names
```

### Annotation File Format

Each annotation file (.txt) contains bounding box information for all objects in the image, with each line formatted as:
```
class_id x_center y_center width height
```
All coordinate values are normalized to the [0, 1] range.

## License

The sample data in this repository follows the original dataset's **CC BY 4.0** license.

Please comply with the following requirements when using:
- **Attribution**: Cite the original paper
- **Academic Use**: Recommended for academic research and learning only
- **Copyright**: Original satellite imagery copyright belongs to data providers

## Citation

If you use this dataset, please cite both the original paper and this repository:

```bibtex
@article{cubaynes2022whales,
  title={Whales from space dataset, an annotated satellite image dataset of whales for training machine learning models},
  author={Cubaynes, Hannah C and Fretwell, Peter T},
  journal={Scientific Data},
  volume={9},
  number={1},
  pages={245},
  year={2022},
  publisher={Nature Publishing Group UK London},
  doi={10.1038/s41597-022-01377-4}
}
```
```bibtex
@article{WANG2025130778,
title = {Whale Identification and Size Estimation in Satellite Imagery via Intelligent Subtle Perception},
journal = {Expert Systems with Applications},
pages = {130778},
year = {2025},
issn = {0957-4174},
doi = {https://doi.org/10.1016/j.eswa.2025.130778},
url = {https://www.sciencedirect.com/science/article/pii/S0957417425043933},
author = {Siqi Wang and Baoxiang Huang and Milena Radenkovic and Ge Chen},
}
```

## Disclaimer

This repository contains personally curated sample data for learning and demonstration purposes only. For the complete dataset usage, please refer to the data availability statement in the original paper.


