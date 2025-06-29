# Food-101 classifier

Computer vision model trained on food-101 dataset

## Navigation

- [Food-101 classifier](#food-101-classifier)
  - [Navigation](#navigation)
  - [Technologies](#technologies)
  - [Local installation](#local-installation)
    - [For developement](#for-developement)
      - [Dataset installation](#dataset-installation)
    - [For inference](#for-inference)
  - [Dataset](#dataset)
    - [Review](#review)
  - [](#)
  - [TODO](#todo)

## Technologies

 - [PyTorch](https://pytorch.org/)
 - [PyTorch Lightning](https://lightning.ai/docs/pytorch/stable/)
 - [Tensorboard](https://www.tensorflow.org/tensorboard)
 - [ONNX](https://onnx.ai/)
 - [FastAPI](https://fastapi.tiangolo.com/)
 - [TensorRT](https://developer.nvidia.com/tensorrt)
 - [uv](https://docs.astral.sh/uv/)
 - [Docker](https://www.docker.com/)

## Local installation

### For developement

#### Dataset installation

1. Download dataset zip archive
    - Download from [Kaggle website](https://www.kaggle.com/datasets/dansbecker/food-101?resource=download)
    - Or via terminal (change download path)
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

## Dataset

### Review

Food-101 paper: https://paperswithcode.com/dataset/food-101

Food-101 on Kaggle: https://www.kaggle.com/datasets/dansbecker/food-101

## 
## TODO

 - [x] start writing todo 
 - [ ] dataset EDA
 - [ ] select model architecture
 - [ ] data processing pipeline
   - [ ] image size
   - [ ] augmentation
 - [ ] convert model to ONNX+TensorRT
 - [ ] make model API
 - [ ] deploy on Docker
