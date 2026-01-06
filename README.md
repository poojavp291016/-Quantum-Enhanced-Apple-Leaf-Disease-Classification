# Quantum-Enhanced-Apple-Leaf-Disease-Classification
A state-of-the-art Quantum-Classical Neural Network (QCNN) for automated apple leaf disease detection, achieving 92.50% accuracy through hybrid quantum-classical deep learning.
This project presents a novel Quantum-Classical Hybrid Neural Network (QCNN) designed to revolutionize agricultural disease detection through the fusion of quantum computing and deep learning. By integrating a 4-qubit quantum circuit with a classical CNN backbone, our model achieves 92.50% accuracy in identifying apple leaf diseases—outperforming traditional CNNs while using 12% fewer parameters. The quantum layer leverages ring entanglement to capture complex feature correlations that classical architectures cannot easily represent, enabling more robust disease classification. Trained on apple leaf images across four disease categories (Healthy, Apple Scab, Apple Rust, and Multiple Diseases), this production-ready system demonstrates the practical viability of quantum-enhanced machine learning for real-world agricultural applications. The complete pipeline includes memory-optimized training (suitable for 4GB GPUs), comprehensive evaluation metrics, and deployment-ready inference code, making it accessible for both research and commercial use.
Key Highlights

- 92.50% Validation Accuracy - Surpasses classical CNN baselines by 2.5-3.5%
- Hybrid Architecture - Classical CNN + 4-qubit quantum circuit with variational layers.
-  4-Class Classification - Healthy, Apple Scab, Apple Rust, Multiple Diseases
  
 Quantum-Classical Neural Network (QCNN) implements a hybrid computational paradigm that synergistically combines classical deep learning with quantum information processing. The architecture is designed based on the principle that classical neural networks excel at hierarchical feature extraction through spatial convolutions, while quantum circuits can capture non-linear feature correlations through quantum entanglement—a phenomenon without classical analog.
Mathematical Formulation
Given an input image X ∈ ℝ^(224×224×3), the QCNN performs the following transformation:
Y = H(Q(A(C(X)))), where:

C(·): Classical CNN feature extractor (spatial → semantic features)
A(·): Attention mechanism (adaptive feature weighting)
Q(·): Quantum feature processor (entanglement-based refinement)
H(·): Hybrid classifier (classical + quantum → predictions)

Architecture Components
1. Classical Feature Extraction Layer
The classical backbone implements a hierarchical feature pyramid through successive convolutional operations with progressively increasing receptive fields:
Stage 1 - Stem Layer:

Applies large-kernel convolution (7×7) with aggressive stride (4) to rapidly downsample input
Maps RGB channels (3) to initial feature space (32 channels)
Operation: X' = ReLU(BatchNorm(Conv₇ₓ₇(X)))
Output dimension: 56×56×32

Stage 2-4 - Residual Blocks:

Each block contains two 3×3 convolutions with batch normalization and ReLU activations
Progressive channel expansion: 32 → 64 → 128 → 224
Spatial downsampling via strided convolutions (factor of 2 per block)
Mathematical form: Fₗ = ReLU(BN(W₂ * ReLU(BN(W₁ * Fₗ₋₁))))
Final dimension: 7×7×224
