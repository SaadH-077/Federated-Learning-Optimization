# 💻🌐 Federated Learning Optimization — Comparative Study of Six Algorithms

A comprehensive course project on **Federated Learning**, evaluating six key algorithms — Centralized Training, FedSGD, FedAvg, SCAFFOLD, FedGH, and FedSAM — across dimensions like convergence, generalization, data heterogeneity, and communication efficiency.

> 🧠 **Course**: Advanced Topics in Machine Learning (ATML - CS)  
> 📅 **Semester**: Spring 2025  
> 🎓 **Institution**: LUMS  
> 👨‍💻 Contributors: Muhammad Saad Haroon, Jawad Saeed, Daanish Uddin Khan

---

## 📦 Project Overview

This assignment explores the design, implementation, and evaluation of **federated learning (FL)** strategies under various non-IID data conditions using the MNIST dataset. Each task investigates a different aspect of FL optimization:

- Task 1: FedSGD vs Centralized Training (Theoretical Equivalence)
- Task 2: FedAvg under varying and extreme heterogeneity
- Task 3: SCAFFOLD — Drift Mitigation via Control Variates
- Task 4: FedGH — Gradient Harmonization to resolve conflicts
- Task 5: FedSAM — Generalization through Sharpness-Aware Minima
- Task 6: Comparative Evaluation & Discussion

---

## 🧪 Algorithms Evaluated

| Algorithm      | Description                                                                 |
|----------------|-----------------------------------------------------------------------------|
| Centralized    | Baseline for upper-bound comparison (access to all data)                   |
| FedSGD         | Federated SGD with one-step gradient averaging                             |
| FedAvg         | Federated Averaging — multi-step local updates                             |
| SCAFFOLD       | Corrects client drift using control variates                               |
| FedGH          | Reduces gradient conflicts through projection/harmonization                |
| FedSAM         | Introduces sharpness-aware minima for better generalization                |

---

## 📊 Dataset

- **MNIST** (Handwritten Digits)
- Federated splits using **Dirichlet Distribution**
- Heterogeneity controlled via **α parameter** (`α = 2.0`, `0.5`, `0.1`)
- Simulated up to 10 clients

---

## 📈 Results Summary

| Dirichlet α | FedAvg (%) | SCAFFOLD (%) | FedGH (%) | FedSAM (%) |
|-------------|------------|---------------|------------|-------------|
| 2.0         | 59.13      | 85.38         | 69.53      | 66.38       |
| 0.5         | 60.23      | 81.55         | 67.47      | 65.35       |
| 0.1         | 38.77      | 64.87         | 43.25      | 60.99       |

✅ **FedSAM** outperforms FedAvg across all settings  
📈 **SCAFFOLD** shows robustness in highly non-IID setups  
⚠️ **FedAvg** struggles in extreme heterogeneity

---

## 📂 Files

| File                                 | Description                                         |
|--------------------------------------|-----------------------------------------------------|
| `FL_Algorithms_Comparison.ipynb`     | Jupyter notebook with full code and experiments     |
| `FL_Algorithms_Comparison.pdf`                | Detailed research-style report with figures/tables  |

---

## 🧠 Key Takeaways

- **Theoretical Equivalence** between FedSGD and centralized training is confirmed under ideal setups.
- **FedAvg** fails under extreme heterogeneity due to conflicting client gradients.
- **SCAFFOLD** successfully mitigates client drift using control variates.
- **FedGH** resolves gradient conflicts, enhancing convergence consistency.
- **FedSAM** generalizes better by targeting flatter regions in the loss landscape using sharpness-aware perturbations.

---

## 📈 Visuals (found in report & notebook)

- Accuracy curves for all models
- Client-wise performance charts
- Gradient conflict graphs (FedGH)
- Sharpness visualizations (FedSAM)
- Comparison of SAM perturbation radii

---

## 💡 Future Work

- Apply these techniques to real-world medical or financial datasets
- Explore **client sampling**, **asynchronous updates**, and **federated personalization**
- Extend to larger architectures (e.g., ResNet, Transformer-based clients)

---

## 🧾 Citation

If referencing this work in academic writing:
```
Muhammad Saad Haroon, Jawad Saeed, Daanish Uddin Khan. "Federated Learning Optimization: A Comparative Analysis." Advanced Topics in Machine Learning, LUMS, Spring 2025.
```

---
> _“A federated model is only as good as its clients are diverse.”_

