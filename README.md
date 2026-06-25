🧠 Model Overview (CNN Architecture)

This project uses a Convolutional Neural Network (CNN) built with TensorFlow / Keras for binary image classification of malaria-infected cells.

The model learns visual patterns from microscopic blood smear images to classify them as:

🟢 Uninfected
🔴 Parasitized
🏗️ Model Architecture

The CNN model follows a deep feature extraction pipeline:

Conv2D (32 filters, 3×3) + ReLU activation
MaxPooling (2×2)
Dropout (to reduce overfitting)
Conv2D (64 filters, 3×3) + ReLU activation
MaxPooling (2×2)
Dropout
Conv2D (128 filters, 3×3) + ReLU activation
MaxPooling (2×2)
Dropout
Flatten Layer (converts feature maps into 1D vector)
Dense Layer (512 units, ReLU activation)
Output Layer (Sigmoid activation) for binary classification
⚙️ Compilation Settings
Optimizer: Adam
Loss Function: Binary Crossentropy
Metric: Accuracy
🏋️ Training Details
Input Image Size: 128 × 128
Batch Training with data augmentation
Epochs: 10
Validation split used for evaluation
📊 Model Performance
✅ Accuracy: ~95%
🎯 High precision and recall for both classes
⚠️ Low false negatives (critical for medical diagnosis)
📉 Well-balanced performance on infected vs uninfected cells
💾 Model Output

The trained model is saved as:

malaria_model.h5
