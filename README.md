# Food-101 classifier

Computer vision model trained on food-101 dataset

## Navigation

- [Food-101 classifier](#food-101-classifier)
  - [Navigation](#navigation)
  - [Dataset](#dataset)
  - [Technologies](#technologies)
    - [Development](#development)
    - [Inference](#inference)
  - [Project structure](#project-structure)
  - [Local installation](#local-installation)
    - [For developement](#for-developement)
      - [Dataset installation](#dataset-installation)
    - [For inference](#for-inference)
  - [TODO](#todo)

## Dataset

Food-101 paper: https://data.vision.ee.ethz.ch/cvl/datasets_extra/food-101/

Food-101 on Kaggle: https://www.kaggle.com/datasets/dansbecker/food-101

> We introduce a challenging data set of 101 food categories, with 101'000 images. For each class, 250 manually reviewed test images are provided as well as 750 training images. On purpose, the training images were not cleaned, and thus still contain some amount of noise. This comes mostly in the form of intense colors and sometimes wrong labels. All images were rescaled to have a maximum side length of 512 pixels.

## Technologies

### Development

 - [uv](https://docs.astral.sh/uv/)
 - [PyTorch](https://pytorch.org/)
 - [PyTorch Lightning](https://lightning.ai/docs/pytorch/stable/)
 - [Tensorboard](https://www.tensorflow.org/tensorboard)
 - [Hydra](https://hydra.cc/)

### Inference 

 - [FastAPI](https://fastapi.tiangolo.com/)
 - [TensorRT](https://developer.nvidia.com/tensorrt)
 - [ONNX](https://onnx.ai/)
 - [Docker](https://www.docker.com/)

## Project structure

```
food101_classifier/
├── src/
│ ├── data/ # Data loaders and transforms
│ ├── models/ # Model architectures
│ ├── training/ # Training loop, LightningModule
│ ├── inference/ # ONNX/TensorRT scripts
│ ├── api/ # FastAPI app
│ └── utils/ # Misc helpers
├── config/ # Hydra configs
├── notebooks/ # EDA and experiments
├── tests/ # Unit tests
├── Dockerfile
├── requirements.txt / pyproject.toml
└── README.md
```

## Local installation

### For developement

#### Dataset installation

1. Download dataset zip archive
 - Option 1: Download from [Kaggle website](https://www.kaggle.com/datasets/dansbecker/food-101?resource=download)
 - Option 2: Or via terminal (change download path)

    ```
    curl -L -o /path/to/download/folder/food-101.zip\
      https://www.kaggle.com/api/v1/datasets/download/dansbecker/food-101
    ```

2. Unzip
    ```
    mkdir -p /path/to/project/data/food-101
    unzip /path/to/download/folder/food-101.zip -d /path/to/project/data/food-101
    ```

### For inference
## TODO

 - [x] start writing todo
 - [ ] set up TensorRT Docker development container
 - [ ] dataset EDA
 - [ ] select model architecture
 - [ ] select evaluation metrics
 - [ ] set up training pipeline
   - [ ] Hydra config handling
   - [ ] lightning dataset
     - [ ] data loading
     - [ ] preprocessing
   - [ ] lightning model
   - [ ] training loop
   - [ ] evaluation loop
   - [ ] tensorboard logging
     - [ ] image grid
     - [ ] loss
     - [ ] accuracy
   - [ ] experiments handling
 - [ ] experiment
   - [ ] try different architectures
   - [ ] try different hyperparameters
   - [ ] compare results
   - [ ] save best model
 - [ ] inference model
   - [ ] convert model to ONNX+TensorRT
   - [ ] make FastAPI api
   - [ ] deploy on Docker
     - [ ] ONNX option
     - [ ] TensorRT option
