🌿 Plant Disease Classification Dataset
📌 Overview

This project uses the New Plant Diseases Dataset for multi-class plant leaf disease classification.

Total Images: ~87,000

Classes: 38

Image Type: RGB leaf images (.jpg)

Task Type: Multi-class image classification

Official Source: Kaggle (Recommended)

The dataset contains high-quality images of healthy and diseased plant leaves across multiple crop species. It is widely used for deep learning research in agricultural disease detection.

📥 Download Links

Kaggle (Official):
https://www.kaggle.com/datasets/vipoooool/new-plant-diseases-dataset

⚠️ Important:
Do NOT commit dataset images to this repository.
Download the dataset locally and place it under the Datasets/ directory as shown below.

🛠 Kaggle Download (CLI)

Install and configure Kaggle API credentials:
https://github.com/Kaggle/kaggle-api#api-credentials

Download dataset:

kaggle datasets download -d vipoooool/new-plant-diseases-dataset


Unzip the dataset and arrange images into the structure below.

📂 Expected Dataset Structure

Create the following structure inside the project root:

Datasets/
  README.md
  train/
    Apple___Apple_scab/
    Apple___Black_rot/
    Apple___Cedar_apple_rust/
    Apple___healthy/
    ...
  val/
    Apple___Apple_scab/
    Apple___Black_rot/
    ...
  test/
    Apple___Apple_scab/
    Apple___Black_rot/
    ...


This layout is fully compatible with:

torchvision.datasets.ImageFolder

🏷 Dataset Characteristics

Multi-class classification problem (38 classes)

RGB leaf images

Balanced dataset (train and validation folders provided)

Includes healthy and diseased leaves

Suitable for:

CNN models

Transfer Learning (ResNet, EfficientNet, MobileNet)

Real-time plant disease detection systems

🌱 Example Plant Categories

The dataset includes diseases from plants such as:

Apple

Corn (Maize)

Tomato

Potato

Grape

Pepper

Strawberry

Peach

Cherry

Each class represents either a specific disease or a healthy leaf condition.

🔍 Usage Example (PyTorch)
from torchvision import transforms
from torchvision.datasets import ImageFolder
from torch.utils.data import DataLoader

transform = transforms.Compose([
    transforms.Resize((224, 224)),
    transforms.ToTensor(),
    transforms.Normalize(mean=[0.485, 0.456, 0.406],
                         std=[0.229, 0.224, 0.225])
])

train_dataset = ImageFolder("Datasets/train", transform=transform)

train_loader = DataLoader(
    train_dataset,
    batch_size=32,
    shuffle=True,
    num_workers=4
)

⚠️ Notes

Ensure:

Train / Validation / Test splits do NOT overlap.

Proper data augmentation is applied (rotation, flip, zoom).

Recommended Techniques:

Transfer Learning

Learning Rate Scheduling

Early Stopping

Model Checkpointing

📜 Acknowledgements / License

Dataset Source: Kaggle – New Plant Diseases Dataset

Intended for academic and research purposes

Refer to the official Kaggle page for licensing and citation requirements.
