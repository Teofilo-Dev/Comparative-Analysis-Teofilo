# Comparative-Analysis-Teofilo

HERE IS MY COLAB LINK : https://colab.research.google.com/drive/1FSMmlgIIBWOTk7H-zWCePElM-kmHQSVp?usp=sharing
A. Model Performance
1. Which pre-trained model achieved the highest accuracy? Why?
  - MobileNetV2 achieved the highest performance with a Test Accuracy of 95.00%. Its architecture is highly efficient for image classification tasks, allowing it to  generalize better on this specific dataset compared to the others.

2 Which model had the lowest performance? What could be the reason?
  - ResNet50 had the lowest performance with a Test Accuracy of only 17.10%. This could be due to vanishing gradients, insufficient training epochs for such a deep architecture, or potential implementation issues as indicated by the high Test Loss of 2.8035.
3. How did loss values compare across models?
  - MobileNetV2 had the lowest Test Loss (0.2312), while ResNet50 had the highest Test Loss (2.8035). VGG16 sat in the middle with a Test Loss of 1.4574.

B. Evaluation Metrics
4. Why is accuracy not enough to evaluate a model?
  - Accuracy can be misleading if classes are imbalanced; it doesn't show if a model is failing completely on specific rare classes while succeeding on common ones.

5. Which model had the best F1-score? What does it indicate?
  - MobileNetV2 had the best F1-score (implied by its 95% accuracy and strong ROC curve). A high F1-score indicates a good balance between precision and recall, meaning the model has low false positives and low false negatives.

6. How did Precision and Recall differ across models?
   - In the MobileNetV2 confusion matrix, most values are on the diagonal, indicating high precision and recall for nearly all classes. ResNet50 showed high recall for only one class (predicting almost everything as "Angel_Wings_Plant") but extremely low precision overall.

C. Confusion Matrix Analysis
7. Which classes were frequently misclassified?
    - In the VGG16 matrix, species like Fire_Orchids and Mangkono were frequently misclassified or missed entirely.

8. What patterns did you observe in the confusion matrix?
   - MobileNetV2 shows a strong diagonal pattern. ResNet50 shows a vertical column pattern, indicating a strong bias where it predicts the same class regardless of the input.

D. ROC and AUC
9. Which model had the highest AUC score?
   - MobileNetV2 had the highest ROC AUC score of 0.99.

10. What does AUC tell us about model performance?
   - AUC (Area Under the Curve) measures the model's ability to distinguish between classes. A score of 0.99 means the model has a 99% chance of correctly distinguishing between a positive and negative instance.

E. Explainability (Grad-CAM)
11. What did Grad-CAM reveal about model decision-making?
   - It showed the specific "attention" regions the model used to classify the image.

12. Did the model focus on relevant image regions?
   - MobileNetV2 focused sharply on the central structure of the plant. VGG16 and ResNet50 had much more scattered attention, often looking at edges or backgrounds.

13. Which model produced the most meaningful heatmaps?
    - MobileNetV2 produced the most meaningful heatmaps, as the highest intensity (white/red) aligned perfectly with the plant's features.

F. Model Comparison & Improvement
14. Which model would you recommend for deployment? Why?
   - MobileNetV2 is recommended because it combines the highest Test Accuracy (95%) with the best AUC (0.99) and the most logical visual focus in Grad-CAM.
15. How can you further improve your best-performing model?
   - Potential improvements include fine-tuning more layers, using data augmentation (rotations, flips) to increase dataset variety, or training for more than 20 epochs.

G. Real-World Application
16. How can your model be applied in real-world scenarios?
    - It can be used in mobile apps for botanists or hobbyists to identify rare flowering plants in the field.

17. What are the risks of deploying an inaccurate model?
    - Deploying a model like ResNet50 (17% accuracy) could lead to dangerous misidentifications, such as mistaking a toxic plant for a safe one.

18. How can this system be integrated into a mobile/web app?
    - The trained models have been saved as .keras and .h5 files. These files can be loaded into a TensorFlow.js or TensorFlow Lite environment for real-time identification via a smartphone camera.

    <img width="1717" height="481" alt="image" src="https://github.com/user-attachments/assets/36401f3a-e22d-41e4-8043-bf03946cd72a" />
    <img width="1681" height="557" alt="image" src="https://github.com/user-attachments/assets/4250c770-7d77-4bcf-aaa7-2ab896069d86" />
    <img width="1685" height="576" alt="image" src="https://github.com/user-attachments/assets/c0f09bd2-fffd-4908-b35e-1ae75815f119" />
    <img width="1078" height="672" alt="image" src="https://github.com/user-attachments/assets/df52ede0-5ba2-4753-a5c2-b84c5532e21b" />



