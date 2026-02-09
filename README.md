# Motor-Component-Alignment-EEG

**Official implementation and dataset** for the paper:  
**"Individual motor-related component alignment enhances EEG decoding accuracy via mitigating across-trial latency variability"**.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## 📄 Abstract
Trial-to-trial latency variability constitutes a fundamental challenge in EEG analysis, in which intrinsic neural fluctuations and cognitive state shifts obscure the temporal fidelity of event-related potentials (ERPs). This temporal jitter creates a smearing effect that primarily degrades endogenous, response-locked components while largely sparing exogenous, stimulus-locked features, thereby compromising across-trial consistency. To resolve this misalignment, we propose a unifying framework for component-wise temporal reconstruction by decomposing single-trial EEG signals with the residual iterative decomposition method, realigning components according to trial-specific intrinsic latencies, and reconstructing temporally coherent ERPs through component recombination. Unlike conventional global or rigid alignment strategies, this framework preserves component-specific temporal dynamics while restoring cross-trial coherence, thereby avoiding the distortions induced by uniform temporal shifts. Validated across unimanual and bimanual motor execution tasks, this method yielded a substantial restoration of signal quality: reconstructed ERPs exhibited a marked amplitude recovery (mean enhancement 4.61 µV) and a profound increase in phase consistency (phase locking value improved by 107%). Crucially, this alignment translated into superior decoding efficacy, accounting for 70% of the performance gain in complex bimanual tasks and boosting unimanual decoding accuracy by 111% compared to sliding-window baselines. These findings underscore that correcting for component-specific latency variability is essential for recovering true neural dynamics. The proposed framework offers a robust and scalable solution for overcoming the intrinsic non-stationarity of EEG, enabling more precise and reproducible neural decoding across diverse experimental tasks.

## 🛠️ Requirements

### Python Environment
The deep learning models (EEGNet, ShallowConvNet, etc.) are implemented in Python.
- Python >= 3.8
- TensorFlow
- NumPy, SciPy, Matplotlib
- scikit-learn

### MATLAB Environment
The preprocessing and RIDE decomposition are implemented in MATLAB.
- MATLAB R2020b or later
- EEGLAB Toolbox
- RIDE Toolbox (included or link to source)

## 📂 Repository Structure

```text
Motor-Component-Alignment-EEG/
├── Data/               # Instructions on how to download/organize data
├── Preprocessing/      # MATLAB scripts for RIDE decomposition and alignment
├── Decoding/           # Python scripts for model training (EEGNet, etc.)
├── Utils/              # Helper functions
├── README.md           # This file
└── LICENSE             # MIT License
