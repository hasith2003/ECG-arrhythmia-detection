Project Overview

This project performs ECG heartbeat classification using deep learning and transfer learning on the MIT-BIH Arrhythmia Database. We classify beats into four AAMI classes (N: Normal, S: Supraventricular, V: Ventricular, F: Fusion), excluding the ambiguous Q class.

Instead of raw ECG signals, we compute STFT representations to capture both time and frequency information. To handle class imbalance, we first tried augmenting STFTs with noise, flipping, and rotation, but these had limited effect, so we applied SMOTE to generate additional samples for underrepresented classes.

We evaluated several transfer learning models:

ResNet

EfficientNet

DenseNet

ConvNeXt — a modern CNN inspired by Transformers, using only convolutions with LayerNorm, GELU, and large kernels.

All models achieved over 90% accuracy, with EfficientNet performing the best. This pipeline demonstrates how time-frequency feature extraction, data balancing, and modern CNNs can be combined for robust ECG arrhythmia detection.
