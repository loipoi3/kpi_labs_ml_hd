### **Evaluation and Explanation of Results**

After performing clustering on raw audio and MFCC-extracted features, the **accuracy results** are:

- **Raw Audio Clustering Accuracy**: **55.56%**
- **MFCC Feature Clustering Accuracy**: **66.67%**

These results indicate that **clustering using MFCC features performs better than clustering on raw audio data**.

---

### **Comparison with the Baseline (Raw Audio Clustering)**
1. **Improved Accuracy with MFCC Features**  
   - Using **MFCC features increased accuracy by ~11%** compared to raw audio clustering.
   - MFCC features help capture key **spectral properties** of the audio, making it easier to differentiate between speakers.

2. **Why Raw Audio Performed Worse?**
   - Raw audio data contains **a lot of unnecessary information** (e.g., noise, pitch variations, non-relevant frequency components).
   - K-Means assumes **spherical clusters**, but raw waveforms can have **complex, non-linear structures** that are harder to separate.

3. **Why MFCC Features Performed Better?**
   - **MFCC compresses the frequency information**, making it **more speaker-dependent**.
   - It helps reduce **irrelevant variability** (e.g., volume differences) and focuses on speech characteristics.
   - As a result, clustering algorithms like **K-Means** can better separate distinct speakers.

---

### **Final Analysis**
- **MFCC-based clustering is a clear improvement over raw audio clustering**.
- **However, 66.67% accuracy is still not perfect**, meaning that:
  - Some clusters **still overlap**.
  - More advanced features (**delta-MFCC, spectrograms**) or different clustering algorithms (**DBSCAN, GMM**) could improve performance.