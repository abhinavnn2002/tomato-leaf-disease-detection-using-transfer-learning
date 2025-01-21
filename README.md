# tomato-leaf-disease-detection-using-transfer-learning


##  Overview
This project focuses on detecting tomato leaf diseases using transfer learning with the ResNet-50 architecture. The primary objective is to compare the performance of two pooling techniques, **Global Average Pooling (GAP)** and **Flatten**, within a model that incorporates a **spatial attention mechanism**. By analyzing the differences in accuracy and performance between these approaches, we aim to determine the optimal configuration for disease detection in tomato leaves.

---

## Key Features
1. **Transfer Learning with ResNet-50**: Leveraged the pre-trained ResNet-50 model to efficiently extract features from the tomato leaf disease dataset.
2. **Spatial Attention Mechanism**: Incorporated a spatial attention layer into the architecture to enhance the model's ability to focus on the most relevant regions of the images.
3. **Pooling Comparison**: Compared the performance of Global Average Pooling (GAP) and Flatten as part of the model pipeline to understand their impact on accuracy and computational efficiency.
4. **Custom Dataset**: Utilized a labeled tomato leaf disease dataset with images of different diseased leaves.
5. **Performance Metrics**: Evaluated and compared the models based on accuracy,confusion matrix.

---

## Methodology
1. **Data Preprocessing**:
   - Resized images to match ResNet-50 input dimensions.
   - Applied data augmentation techniques such as rotation, flipping, and normalization to improve generalization.

2. **Model Architecture**:
   - Base model: ResNet-50 with pre-trained ImageNet weights.
   - Added a spatial attention layer after feature extraction to focus on critical regions of the images.
   - Tested two variants of pooling layers:
     - **Global Average Pooling (GAP)**
     - **Flatten**

3. **Training**:
   - Optimized the models using the Adam optimizer and categorical cross-entropy loss.
   - Split the dataset into training, validation, and testing sets.
   - Trained models for 25 epochs with early stopping based on validation loss.

4. **Comparison**:
   - Compared GAP and Flatten-based models by analyzing accuracy and loss curves.
   - Conducted statistical analysis to quantify the difference in performance.

---

## Results
- **GAP vs. Flatten**:
  - GAP outperformed Flatten by achieving **10% higher accuracy** in the tomato leaf disease detection task.
  - GAP demonstrated better generalization and reduced overfitting compared to Flatten.
- **Spatial Attention Effectiveness**:
  - Improved the model's ability to detect diseases by emphasizing relevant image regions.



---

## Technologies Used
- **Frameworks and Libraries**: TensorFlow, Keras, NumPy, Matplotlib
- **Hardware**: GPU-accelerated training using colab pro
- **Dataset**: Custom tomato leaf disease dataset

---

## Conclusion
This project highlights the effectiveness of combining transfer learning with spatial attention for tomato leaf disease detection. The comparison between GAP and Flatten pooling methods revealed that GAP provides superior performance, making it a better choice for similar tasks. The findings can guide future research and applications in agricultural disease detection using deep learning.

