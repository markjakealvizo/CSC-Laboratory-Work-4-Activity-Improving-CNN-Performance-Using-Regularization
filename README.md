# CSC-Laboratory-Work-4-Activity-Improving-CNN-Performance-Using-


Google Collab link:https://colab.research.google.com/drive/1d5w8S6yCnHnfjHXTUlbsZ4sU_tHwl3VJ#scrollTo=fmp0WQ7OD5lK

## PART 4: Compare Results (Before vs After)
Students must create a comparison table

<img width="628" height="412" alt="image" src="https://github.com/user-attachments/assets/25f38c07-67ad-47a6-b2a4-ed1db5d5535b" />


## GUIDE QUESTIONS (Student Explanation & Reflection)
### A. Model Evaluation Analysis

1. What were the weakest-performing classes based on the confusion matrix?

**Answer:** 
Juneberry (~0.45 recall)

Pink trumpet tree (~0.52 recall)

Mediterranean Cypress Tree (~0.62 recall)

Estern Redbud (~0.61 recall)

Olive tree (~0.69 recall) (borderline weak)


2. How did Precision, Recall, and F1-score vary across classes?

**Answer:** Precision, recall, and F1-score varied across classes, indicating that the model performed better on some categories than others. Precision was generally moderate to high, showing that many predictions were correct, while recall fluctuated more, meaning some classes were not detected as consistently. As a result, F1-scores also varied, with most classes achieving reasonable balance but a few showing weaker overall performance due to either lower precision or recall. Overall, the model demonstrated fairly good but uneven performance across different classes.

3. What does a low recall indicate in your model?

**Answer:** A low recall indicates that the model is missing many actual instances of a class, meaning it produces a high number of false negatives. In other words, even when the object or class is present, the model հաճախ fails to detect or correctly classify it. This suggests the model may be too conservative or struggles to distinguish that class from others, leading to incomplete detection performance.

4. How does AUC score reflect model performance compared to accuracy?

**Answer:** The AUC score measures how well the model separates classes across all thresholds, while accuracy shows how many predictions are correct at a fixed threshold. Here, the high AUC (0.95) suggests strong class discrimination, even though the accuracy (76%) is lower due to misclassifications at the chosen threshold.

### B. Model Improvement


5. How did data augmentation affect validation accuracy?

**Answer:** Data augmentation improved validation accuracy by helping the model generalize better to unseen data. By exposing the model to varied versions of the training images (e.g., rotations, flips), it reduced overfitting, which is reflected in the relatively strong validation accuracy (~76%) compared to training performance.

6. Why is Batch Normalization important in CNNs?

**Answer:** Batch Normalization is important in CNNs because it stabilizes and speeds up training by normalizing layer inputs, which reduces internal covariate shift. It also allows the model to use higher learning rates and improves generalization, often leading to better and more consistent performance.

7. What role did Dropout play in improving your model?

**Answer:** Dropout helped improve the model by reducing overfitting. During training, it randomly deactivates some neurons, which forces the network to learn more robust and general features instead of relying too heavily on specific patterns. This leads to better performance on unseen data and improved generalization.

8. How did Early Stopping prevent overfitting?

**Answer:** Early stopping prevented overfitting by monitoring validation performance during training and stopping the process when it stopped improving. This ensures the model does not continue training and start learning noise from the training data, helping it maintain better generalization on unseen data.


### C. Performance Comparison


9. What improvements were observed after modifying the model?

**Answer:** After modifying the model, performance improved significantly, with higher validation accuracy and better balance between precision and recall across classes. The model became more stable and generalized better to unseen data, showing reduced overfitting and stronger overall classification performance.

10. Which enhancement contributed the most to performance improvement? Why?

**Answer:** The combination of data augmentation and transfer learning likely contributed the most to the performance improvement. Data augmentation helped the model generalize better by exposing it to varied versions of the same images, reducing overfitting. Transfer learning provided strong pretrained feature extraction, allowing the model to learn meaningful patterns more quickly and effectively, which significantly boosted validation performance.

11. Did the gap between training and validation accuracy decrease? Explain.

**Answer:** Yes, the gap between training and validation accuracy decreased after the improvements. This indicates reduced overfitting, meaning the model became better at generalizing rather than just memorizing training data. As a result, training and validation performances became more consistent.

### D. Explainability (Grad-CAM Integration)


12. How did Grad-CAM help in understanding model predictions?

**Answer:** Grad-CAM helped by highlighting the regions of an image that the model focused on when making a prediction. This made it easier to understand whether the model was looking at meaningful parts of the tree (like leaves or shape) or irrelevant background areas, improving interpretability of its decisions.

13. Did the improved model focus on more relevant regions? Provide evidence.

**Answer:** Yes, the improved model focused on more relevant regions. The Grad-CAM visualization shows strong activation over the leaf structures and central parts of the tree, which are important for classification, while still giving minimal attention to the background areas like the sky. This indicates that the model is learning to base its predictions on meaningful visual features rather than irrelevant surroundings.

**Evidence:**

<img width="389" height="411" alt="image" src="https://github.com/user-attachments/assets/a254fc60-340e-4d54-9841-b4cce9d66818" />


14. Why is explainability important in real-world AI applications?

**Answer:** Explainability is important in real-world AI because it helps users understand how and why a model makes decisions. This builds trust, makes it easier to detect errors or biases, and ensures the model is behaving correctly, especially in high-stakes applications like healthcare, finance, or safety-related systems.
