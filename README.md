# Pneumonia-Detection-Using-Machine-Learning
-Overview
This project focuses on developing a Pneumonia Detection System using deep learning techniques, specifically leveraging the VGG16 architecture pre-trained on ImageNet. The model is designed to classify chest X-ray images into three categories:

Bacterial Pneumonia
Viral Pneumonia
Normal
The system applies image preprocessing, model training, evaluation, and finally deploys a web application to classify X-ray images.

Project Structure
Data Preprocessing
The input data is preprocessed using ImageDataGenerator. Key preprocessing steps include:

Rescaling pixel values.
Shear transformation.
Zoom augmentation.
Model Architecture
The core of this project is the VGG16 architecture, which is pre-trained on the ImageNet dataset. The convolutional layers are frozen, and a custom dense layer is added for classification.

Loss Function: Categorical Cross-Entropy.
Optimizer: Adam.
Metrics: Accuracy.
Training and Fine-tuning
The model is trained on the augmented dataset to minimize overfitting and improve accuracy. The process includes:

Logging training metrics such as accuracy, loss, and time taken.
Saving the trained model for future usage.
Model Evaluation
The trained model is evaluated on a preprocessed test dataset, computing:

Precision
Recall
F1-score
Confusion matrix
Deployment
The model is deployed as a web application using Streamlit. Users can input the URL of a chest X-ray image, which will be classified in real time.

Dataset
We used the chest X-ray dataset from Kaggle for model training and evaluation.

Chest X-ray Pneumonia Dataset

Installation and Setup
To set up the project locally:

Clone the repository:
git clone <repository_url>
Install required packages:
pip install -r requirements.txt
Download the dataset from the provided link, extract it, and place it in the corresponding folder:
/data
Run the training script to start training the model:
python train.py
For deploying the web application, use:
streamlit run app.py
Project Files
train.py: Script for training the model.
evaluate.py: Script for model evaluation.
app.py: Web application for real-time X-ray classification.
params.yaml: Configuration file.
requirements.txt: List of dependencies.
Results
The system achieves promising results with high accuracy, precision, and recall in detecting pneumonia from X-ray images.

Future Work
Future improvements could include:

Exploring additional architectures like ResNet.
Expanding the categories to include other respiratory conditions.
Improving the deployment process for scalability.
