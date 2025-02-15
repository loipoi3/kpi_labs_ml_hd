## Evaluation and Results Comparison

This section provides an evaluation of the performance of our two models and compares the baseline CNN with the fine-tuned ResNet18.

### Baseline CNN (Trained from Scratch)
- **Test Accuracy:** 84.63%
- **Training Loss:**  
  - The loss decreased gradually from approximately 0.95 to 0.35 over 5 epochs.
- **Observations:**  
  - The baseline model, while simple (with three convolutional layers), was able to learn useful features from the dataset.
  - Its limited depth means that it might not capture the more complex patterns present in the images.

### Fine-Tuned ResNet18
- **Test Accuracy:** 92.23%
- **Training Loss:**  
  - The loss dropped rapidly from around 0.28 to 0.06 over 5 epochs.
- **Observations:**  
  - Leveraging a ResNet18 model pretrained on ImageNet provided a strong starting point.
  - The pretrained features allowed the network to adapt quickly to our dataset, leading to faster convergence and improved accuracy.
  - The deeper architecture with residual connections enabled the model to extract more complex and robust features compared to the baseline CNN.

### Comparison and Conclusion
- **Accuracy Improvement:**  
  Fine-tuning ResNet18 resulted in an improvement of about **7.6 percentage points** in test accuracy compared to the baseline CNN.
  
- **Learning Efficiency:**  
  The fine-tuned ResNet18 converged much faster due to its pretrained weights, while the baseline CNN took longer to learn useful representations.
  
- **Model Capacity:**  
  The enhanced depth and the use of residual connections in ResNet18 allowed it to capture more intricate visual features than the simpler CNN architecture.

**Final Takeaway:**  
For this task, leveraging transfer learning with a pretrained ResNet18 proved to be highly effective. Not only did it achieve a higher accuracy (92.23% vs. 84.63%), but it also converged faster and demonstrated better generalization to the test data. This makes fine-tuning a powerful approach for computer vision tasks, especially when working with moderate-sized datasets.

---