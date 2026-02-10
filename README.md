
# AB6 – Towards Smarter Agriculture: Deep Learning-Based Multistage Detection of Leaf Diseases

## Team Info
- 22471A0533 — **KOYYALAMUDI VENKATA RAMESH** ( [LinkedIn](https://linkedin.com/in/xxxxxxxxxx) )
_Work Done: Project lead and coordinator, Designed overall system architecture, Implemented EfficientNet-B0 model using transfer learning, Managed model training, testing, and result analys

- 22471A0557 — **BANGARU SURYA PRASAD** ( [LinkedIn](https://www.linkedin.com/in/surya-bangaru-4b243a374/) )
_Work Done: Dataset collection and class selection from PlantVillage, Data preprocessing and augmentation, Assisted in model evaluation and performance comparison

- 22471A0561 — **THULLIBILLI NAGAIAH** ( [LinkedIn](https://www.linkedin.com/in/nagaiah-thullibilli-8724a93a6/) )
_Work Done: Image preprocessing pipeline implementation (resizing, normalization, denoising), Exploratory Data Analysis (EDA), Visualization of dataset distribution and results

- 22471A0547 — **SHAIK ABDUL NABI** ( [LinkedIn](https://www.linkedin.com/in/abdul-nabi-24ba2628b/) )
_Work Done: Segmentation logic and post-processing, Performance metrics computation (Precision, Recall, F1, AUC), Documentation and report preparation

---

## Abstract
Farmers are currently facing a dilemma in identifying plant pathogens. Why is this? Using image data from plant leaves, scientists are currently exploring ways to use deep learning to identify plant-related diseases. PlantVillage Dataset is being utilized in this project to showcase approximately 38 categories of plant leaves. However, for better training and evaluation, only 10 classes with 200 images each were selected to ensure balanced learning. The preprocessing techniques for image size and CLAHE are the first ones. These steps help in enhancing image quality and bringing out clearer disease features. Features are extracted from the images using PCFAN. We used CV2 (Computer Vision 2), and EfficientNet B0 is used to pinpoint specific illnesses. The model was trained using transfer learning and achieved strong classification accuracy of 97.9% on the testing dataset and 96.2% accuracy on unseen validation data. Evaluation metrics like precision, recall, and F1-score consistently remained above 95% across all disease categories. Red Fox Optimization is used for the precise segmenting of affected areas, improving the focus on diseased regions and achieving segmentation accuracy above 94%. This overall approach supports early and reliable disease identification in plants.

---

## Paper Reference (Inspiration)
👉 **[Paper Title xxxxxxxxxx
  – Author Names xxxxxxxxxx
 ](Paper URL here)**
Original conference/IEEE paper used as inspiration for the model.

---

## Our Improvement Over Existing Paper
xxxxxxxxxx

---

🧩 About the Project
What the Project Does

This project automatically detects and classifies plant leaf diseases from images using deep learning and highlights the affected regions.

Why It Is Useful

Enables early disease detection

Reduces dependency on agricultural experts

Helps farmers take timely preventive measures

Supports smart and precision agriculture

🔁 General Project Workflow

Input Leaf Image
→ Image Preprocessing
→ Feature Extraction
→ EfficientNet-B0 Model
→ Disease Classification
→ Segmentation of Diseased Region
→ Final Output (Disease type + affected area)

📊 Dataset Used
👉 PlantVillage Dataset
🔗 https://www.kaggle.com/datasets/emmarex/plantdisease
Dataset Details
Total Images: ~89,000
Number of Classes: 38 (10 selected for this project)
Images per Class Used: 200
Image Type: RGB leaf images
Includes healthy and diseased plant leaves

🧰 Dependencies Used
Python
TensorFlow / Keras
OpenCV (cv2)
NumPy
Matplotlib
scikit-learn

🔍 EDA & Preprocessing
Dataset class distribution analysis
Images resized to 224×224
Pixel normalization applied
CLAHE used for contrast enhancement
Noise removal and grayscale conversion
Data augmentation (flip, rotation)
Removal of duplicate and corrupted images

🧪 Model Training Info
Model: EfficientNet-B0
Training Type: Supervised learning
Transfer learning with pretrained weights
Optimizer: Adam
Loss Function: Categorical Cross-Entropy
Training–Validation–Test split applied
Training performed using Google Colab (GPU)

🧾 Model Testing / Evaluation
Metrics Used
Accuracy
Precision
Recall
F1-score
ROC–AUC
Confusion Matrix
Evaluation was conducted on unseen test data to ensure generalization.

🏆 Results
Test Accuracy: 97.9%
Validation Accuracy: 96.2%
Average Precision: 96%
Average Recall: 94.2%
Average F1-score: 95%
Segmentation Accuracy: >94%
Strong performance across all disease classes

⚠️ Limitations & Future Work
Limitations
Trained on controlled dataset images
Some disease classes have similar visual patterns
Outdoor field conditions not included
Future Work
Test the system on real-world farm images
Deploy the model on mobile applications
Improve segmentation accuracy further
Extend to more crop types and diseases

---
