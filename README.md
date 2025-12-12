# ml_assignment
# machinelearning_individualassignment
# Dropout and Regularization in Neural Networks

**Author:** Padma Sri Veeramachaneni  
**Course:** Machine Learning Tutorial (Individual Assignment)  
**University:** University of Hertfordshire  
**Framework:** PyTorch  

---

## 📚 Overview

This repository contains a comprehensive tutorial exploring how dropout regularization prevents overfitting in neural networks. Through hands-on experimentation with the Breast Cancer Wisconsin dataset, I demonstrate how different dropout rates affect model performance, decision boundaries, and generalization capabilities.

## 🎯 What You'll Learn

This tutorial investigates three key aspects of dropout regularization:

1. **Overfitting Prevention** - How dropout helps neural networks generalize better to unseen data
2. **Training Dynamics** - Analysis of loss and accuracy curves across different dropout rates
3. **Decision Boundaries** - Visual comparison of how regularization shapes learned patterns

## 🔬 Methodology

### Dataset
- **Source:** Breast Cancer Wisconsin (Diagnostic) Dataset
- **Task:** Binary classification (Malignant vs. Benign tumors)
- **Preprocessing:** 
  - Standardization using StandardScaler
  - Dimensionality reduction via PCA (30 features → 2 components)
  - Train/Test split (80/20)

### Experiments
I trained identical neural network architectures with only ONE variable changed:

| Experiment | Dropout Rate | Purpose |
|------------|--------------|---------|
| No Dropout | 0.0 | Baseline (prone to overfitting) |
| Light Dropout | 0.2 | Mild regularization |
| Standard Dropout | 0.5 | Common practice in deep learning |
| Heavy Dropout | 0.7 | Aggressive regularization |

### Network Architecture
 **Fixed Parameters:**
- Optimizer: Adam (learning rate = 0.001)
- Loss Function: Binary Cross-Entropy with Logits
- Training Epochs: 100
- Batch Size: 32

## 📊 Key Findings

### 1. Overfitting Behavior

My experiments revealed clear patterns in how dropout affects the train-test performance gap:

- **No Dropout (0.0):** 
  - Train Accuracy: 95.6%
  - Test Accuracy: 93.0%
  - **Gap: 2.6%** ← Clear sign of overfitting
  
- **Light Dropout (0.2):**
  - Train Accuracy: 96.3%
  - Test Accuracy: 94.7%
  - **Gap: 1.5%** ← Improved generalization

- **Standard Dropout (0.5):**
  - Train Accuracy: 95.6%
  - Test Accuracy: 94.7%
  - **Gap: 0.9%** ← Best balance

- **Heavy Dropout (0.7):**
  - Train Accuracy: 95.4%
  - Test Accuracy: 94.7%
  - **Gap: 0.6%** ← Risk of underfitting

### 2. Decision Boundary Analysis

The visualizations show that:
- Without dropout, the model creates **complex, wiggly boundaries** that memorize training noise
- With dropout, boundaries become **smoother and more generalizable**
- Excessive dropout (0.7) may create **oversimplified boundaries**

### 3. Training Stability

Loss curves demonstrate:
- Models without dropout show diverging train/test loss over time
- Dropout creates more stable convergence where both losses decrease together
- Standard dropout (0.5) provides optimal balance

## 🚀 Quick Start

### Requirements
 ## 🎓 Educational Value

This tutorial is designed for:
- **Students** learning about neural network regularization techniques
- **Practitioners** wanting to understand when and how to apply dropout
- **Researchers** needing visual comparisons of regularization effects

### Prerequisites
- Basic understanding of neural networks
- Familiarity with Python and PyTorch
- Understanding of overfitting concepts

## 💡 Practical Recommendations

Based on my experimental findings:

| Dropout Rate | Best Use Case | When to Use |
|--------------|---------------|-------------|
| **0.0 - 0.2** | Small datasets, simple problems | When training is fast and you need max performance |
| **0.3 - 0.5** | General purpose, most problems | Default choice for hidden layers |
| **0.6 - 0.8** | Large networks, complex data | When significant overfitting is observed |

**Best Practices:**
1. Start with 0.5 for hidden layers (industry standard)
2. Use 0.2-0.3 for input layers if needed
3. Never apply dropout to output layers
4. Combine with other techniques: L2 regularization, batch normalization, early stopping
5. Monitor the train-test gap as your primary metric

## 📖 References

This tutorial builds upon foundational research in dropout regularization:

1. Srivastava, N., Hinton, G., Krizhevsky, A., Sutskever, I., & Salakhutdinov, R. (2014). **Dropout: A Simple Way to Prevent Neural Networks from Overfitting.** *Journal of Machine Learning Research*, 15(56), 1929-1958.

2. Goodfellow, I., Bengio, Y., & Courville, A. (2016). **Deep Learning** (Chapter 7: Regularization for Deep Learning). MIT Press.

3. UCI Machine Learning Repository. **Breast Cancer Wisconsin (Diagnostic) Data Set.** Retrieved from https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+(Diagnostic)

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

 ## 🤝 Contributing

While this is an individual assignment, I welcome feedback and suggestions! Feel free to:
- Open an issue for bugs or questions
- Submit pull requests for improvements
- Share your own experiments with different datasets



## 🙏 Acknowledgments

- University of Hertfordshire for course guidance
- PyTorch community for excellent documentation
- UCI Machine Learning Repository for providing the dataset
- Original dropout paper authors for pioneering this technique

