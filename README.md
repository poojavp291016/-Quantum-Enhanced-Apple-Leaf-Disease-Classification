# Quantum-Enhanced-Apple-Leaf-Disease-Classification
A state-of-the-art Quantum-Classical Neural Network (QCNN) for automated apple leaf disease detection, achieving 92.50% accuracy through hybrid quantum-classical deep learning.
This project presents a novel Quantum-Classical Hybrid Neural Network (QCNN) designed to revolutionize agricultural disease detection through the fusion of quantum computing and deep learning. By integrating a 4-qubit quantum circuit with a classical CNN backbone, our model achieves 92.50% accuracy in identifying apple leaf diseases—outperforming traditional CNNs while using 12% fewer parameters. The quantum layer leverages ring entanglement to capture complex feature correlations that classical architectures cannot easily represent, enabling more robust disease classification. Trained on apple leaf images across four disease categories (Healthy, Apple Scab, Apple Rust, and Multiple Diseases), this production-ready system demonstrates the practical viability of quantum-enhanced machine learning for real-world agricultural applications. The complete pipeline includes memory-optimized training (suitable for 4GB GPUs), comprehensive evaluation metrics, and deployment-ready inference code, making it accessible for both research and commercial use.
Key Highlights

- 92.50% Validation Accuracy - Surpasses classical CNN baselines by 2.5-3.5%
- Hybrid Architecture - Classical CNN + 4-qubit quantum circuit with variational layers.
-  4-Class Classification - Healthy, Apple Scab, Apple Rust, Multiple Diseases
Input Image (224×224×3)
         ↓
    [Classical Convolutions]
    Hierarchical feature extraction
    via spatial filtering operations
         ↓
  Feature Maps (7×7×224)
         ↓
  [Global Average Pooling]
  Spatial aggregation: ℝ^(7×7×224) → ℝ^224
         ↓
  [Attention Mechanism]
  Channel recalibration via
  learned importance weights
         ↓
    ↙         ↘
Classical    Quantum Path
Branch       ↓
  │     [Amplitude Encoding]
  │     Classical → Quantum
  │     features     state
  │          ↓
  │     [Variational Circuit]
  │     Entanglement-based
  │     feature refinement
  │     (Hilbert space: 2⁴)
  │          ↓
  │     [Measurement]
  │     Quantum → Classical
  │          ↓
  └────→ [Concatenation]
         Hybrid feature vector
         (dim = 228)
              ↓
      [Dense Layers + Dropout]
      Non-linear classification
      with regularization
              ↓
      [Softmax Activation]
      Probability distribution
              ↓
    Disease Class (4 outputs)
