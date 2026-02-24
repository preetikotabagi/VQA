Medical Visual Question Answering (VQA)

Problem Statement:
The goal of this project is to build a Medical Visual Question Answering (VQA) system.

The system takes:
1. A radiology image
2. A clinical question related to the image

And predicts:
The correct answer based on the image.

Example:
Image + Question → Answer
"Is there a fracture?" → "No"

Dataset Used:
Dataset Name: VQA-RAD (Visual Question Answering in Radiology)
Training Samples: 1793
Test Samples: 451
The dataset contains medical radiology images along with corresponding clinical question–answer pairs.

Models Used:

Text Embedding Model:
BERT-base (bert-base-uncased)
Used to convert clinical questions into text embeddings.

Vision Encoding Model:
ResNet-50 (ImageNet pre-trained)
Used to extract visual features from medical images.

Fusion Method:
The image features and question embeddings are combined (concatenated).
The combined features are passed through a classifier to predict the answer.

Training Details:
Transfer Learning was used.
Pre-trained BERT and ResNet-50 were fine-tuned on the VQA-RAD dataset.
The problem was formulated as a multi-class classification task.
Top-50 most frequent answers were used along with one "unknown" class.
Optimizer: AdamW
Loss Function: CrossEntropyLoss

Results:
Epoch 1:
Test Accuracy: 65.19%

Epoch 2:
Test Accuracy: 67.41% (Best Performance)

Epoch 3:
Test Accuracy: 65.63%

Best Test Accuracy Achieved: 67.41%
Overfitting was observed after Epoch 2.

Author:
Preeti Kotabagi

Computer Science Engineering
