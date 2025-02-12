
# Fusion of Spatial and Temporal Features with Transformer Gates: A Hybrid Deep Learning Model for Intrusion Detection in Systems

A hybrid deep learning model combining **CNNs**, **LSTMs**, and **Transformer gates** for robust intrusion detection using the UNSW-NB15 dataset. Achieves **90.81% accuracy** in binary classification and addresses challenges like class imbalance and spatiotemporal pattern overlap.

## Key Features
- **Hybrid Architecture**: Fuses spatial (CNN) and temporal (LSTM) features via Transformer gates.
- **Advanced Preprocessing**: Handles class imbalance, feature engineering, and outlier detection.
- **Data Transformation**: Converts network traffic into sequences/images for multimodal learning.
- **State-of-the-Art Results**: 0.9781 AUC in binary classification, 81.22% multiclass accuracy.

## Installation
```bash
git clone https://github.com/yourusername/fusion-spatial-temporal-transformer.git
cd DeepHybrid-IDS-Cyberattack-Classification
pip install -r requirements.txt
```

## Model Architecture

### Core Components:
1. **Multi-Scale CNN**: Dilated convolutions capture spatial patterns.
2. **Bidirectional LSTM**: Processes temporal sequences.
3. **TransformerFusion**: Gates integrate CNN/LSTM features using multi-head attention.
4. **Classification Head**: Dense layers with Swish activation and dropout.

## Dataset
**UNSW-NB15 Dataset** - Contains 49 network traffic features across 10 classes:
- Normal traffic
- 9 attack categories (DoS, Exploits, Fuzzers, etc.

**Preprocessing Steps**:
- Class balancing (remove <5% minority classes)
- Feature engineering (loss metrics, TCP patterns)
- Boruta-based feature selection
- Sequence/image transformation

## Results
| Model Type       | Accuracy | F1-Score | AUC    |
|------------------|----------|----------|--------|
| Multiclass       | 81.22%   | 78.09%   | 0.9766 |
| Binary (Attack vs Normal) | 90.81% | 90.81%   | 0.9781 |

**Key Insights**:
- 92.8% attack recall in binary mode
- Challenges with class overlap (e.g., Analysis vs Reconnaissance)

## Contributing
Contributions welcome! Please:
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/your-feature`)
3. Submit a Pull Request

## License
MIT License - See [LICENSE](LICENSE) for details.

## References
- Singh & Jang-Jaccard (2022) - Multi-scale CNN approach
- Moustafa & Slay (2011) - UNSW-NB15 dataset
- Acharya et al. (2023) - CNN-BiLSTM hybrid model

**Contact**: Eduardo Fontes Baltazar da Silveira - eduardosilveira@ufba.br

