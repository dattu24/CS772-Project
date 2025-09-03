# Learning What Matters: Prioritized Data Selection for Improving Model Generalization

## Description
This project enhances the RHO-LOSS framework(https://arxiv.org/abs/2206.07137) for prioritized data selection in deep learning. The goal is to improve model generalization and training efficiency by dynamically selecting training samples that are most informative, diverse, and uncertain.

## Key Features
- **DivBS + RHO-LOSS**: Integrates gradient-based diversity to reduce redundant samples, reaching 80% CIFAR-10 accuracy by epoch 36.
- **EMA-Adaptive RHO**: Dynamically adjusts sample selection based on exponential moving average of reducible loss, reducing forward-backward passes by 2.8%.
- **Entropy-Regularized RHO**: Balances reducible loss with predictive uncertainty, achieving faster convergence with β = 0.7.
- **RHO-LOSS + BALD**: Combines reducible loss and Bayesian uncertainty, improving 80% accuracy milestone by 6 epochs.
- **Hybrid Diversity Selection**: Penalizes only maximum similarity to selected samples, reaching 80% accuracy in 38 epochs with λ = 0.3.
- **Class-Balanced RHO-DCAST**: Adjusts selection per class to handle imbalance, hitting 80% accuracy by epoch 34 with λ = 0.2.

## Results
| Method                   | Epoch to 80% Accuracy |
|--------------------------|-----------------------|
| Baseline RHO-LOSS        | 41                    |
| DivBS + RHO-LOSS         | 36                    |
| EMA-Adaptive RHO         | 41                    |
| Entropy-RHO (β = 0.7)    | 37                    |
| RHO + BALD               | 35                    |
| Hybrid Diversity (λ=0.3) | 38                    |
| Class-Balanced (λ=0.2)   | 34                    |


## License
This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.
