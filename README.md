# Deep Learning – From Neural Networks to Image Classification 🧠

A collection of my deep learning experiments and image classification work developed for **FIT3181: Deep Learning at Monash University**.

This project covers different stages of deep learning, starting from understanding how neural networks work, implementing and training CNNs, and eventually fine-tuning pretrained vision models for a Kaggle image classification competition.

Throughout the assignment, I experimented with different architectures, training techniques and optimisation methods to understand how they affect model performance.

## 🎯 Project Highlights

| Achievement | Result |
|---|---|
| FIT3181 Assignment 1 | **100%** |
| Kaggle leaderboard score | **95.03%** |
| Mean 5-fold validation accuracy | **99.69%** |
| Kaggle classification task | **20 classes** |

*The Kaggle score is based on my submitted report. Validation accuracy was measured on the training dataset's held-out folds, not the Kaggle test set.*

## 🔬 Part 1 – Deep Learning Fundamentals

The first part focuses on understanding how neural networks work behind the scenes.

Topics covered include:
- Activation functions and their derivatives.
- Forward propagation and backpropagation.
- Neural network parameter updates and optimisation.
- Understanding how model weights are adjusted during training.

This helped me strengthen my understanding of the mathematical foundations behind deep learning.

## ⚙️ Part 2 – Deep Neural Networks

In this part, I implemented feed-forward neural networks using **PyTorch** and experimented with the Fashion-MNIST dataset.

Some of the techniques explored include:

- Hyperparameter tuning using grid search.
- Different activation functions and hidden-layer configurations.
- Cross-entropy with entropy regularisation.
- Sharpness-Aware Minimisation (SAM).

The main objective was to understand how model architecture and optimisation techniques influence training and generalisation.

## 🖼️ Part 3 – CNN and Image Classification

This part focuses on building and evaluating Convolutional Neural Networks for image classification.

I implemented a configurable CNN and experimented with several techniques:

| Technique | Purpose |
|---|---|
| Mixup | Mix training images and labels to improve generalisation |
| CutMix | Combine image regions and labels during training |
| One-vs-All (OVA) | Explore an alternative classification loss |
| Rotation-based self-supervised learning | Learn additional image representations through rotation prediction |

One interesting observation was that more advanced techniques did not always produce better validation accuracy. Some experiments performed worse than the baseline CNN, showing the importance of evaluating techniques rather than assuming they will always improve results.

## 🏆 Kaggle Image Classification

For the Kaggle component, I worked on a **20-class image classification problem** involving labelled training images and an unseen test dataset.

After experimenting with different approaches, I used a pretrained **DFN5B CLIP ViT-H/14-378** vision model through OpenCLIP.

The workflow included:

1. Preparing the image datasets and applying augmentation.
2. Training a classification head on pretrained visual features.
3. Fine-tuning selected model layers.
4. Performing five-fold stratified cross-validation.
5. Combining predictions from multiple folds through model ensembling.
6. Generating the final Kaggle submission.

The final approach achieved **99.69% mean validation accuracy** and a **95.03% Kaggle leaderboard score**.

The difference between validation and Kaggle performance also highlighted the importance of generalisation when working with unseen data.

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Python | Programming language |
| PyTorch | Deep learning model development |
| Torchvision | Datasets and image transformations |
| OpenCLIP | Pretrained vision model |
| NumPy & pandas | Data processing |
| Scikit-learn | Cross-validation |
| Matplotlib | Training visualisation |
| Google Colab | GPU-based model training |
| Kaggle | Model evaluation |

## 📂 Repository Structure

**assignment/**
- Part 1 – Deep learning fundamentals and theory.
- Part 2 – Feed-forward neural networks and optimisation.
- Part 3 – CNN architectures and image classification experiments.

**kaggle/**
- Kaggle notebook containing the CLIP fine-tuning, five-fold training, ensembling and submission workflow.

## 🚀 Running the Notebooks

The notebooks were developed using Python and PyTorch, primarily in Google Colab.

To explore the project:

1. Download or clone this repository.
2. Open the relevant notebook in Google Colab or Jupyter.
3. Install the required Python libraries.
4. Prepare the relevant datasets and update their file paths.
5. Use a GPU runtime for model training.

The university-provided image datasets and pretrained model checkpoints are not included in this repository. Running the complete experiments requires access to the relevant datasets and sufficient computational resources.

## 💡 What I Learned

This assignment helped me better understand both the theory and practical implementation of deep learning.

I learned that achieving good performance is not just about selecting a powerful model. Data preparation, augmentation, optimisation, evaluation and model selection all play important roles.

Working on the Kaggle competition was particularly interesting because it allowed me to apply what I learned to unseen images and explore how pretrained vision models can improve classification performance.

## 📚 Project Information

**Course:** FIT3181 – Deep Learning

**University:** Monash University

**Year:** 2026

**Developer:** Khoo Lynn

**Assignment 1 Result:** 100%

This project was developed for academic and learning purposes.
