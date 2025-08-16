# DCR Evaluator

A comprehensive evaluation framework for Deep Concept Reasoning (DCR) applied to tabular data classification tasks.

## Overview

This repository implements a systematic evaluation of Deep Concept Reasoning (DCR), a neural-symbolic approach that enhances the interpretability of machine learning decisions by applying logical rules to concept abstractions derived from data. The evaluation includes comparative analysis with state-of-the-art machine learning models and a real-world application to credit risk scoring.

## Key Features

- **Comprehensive Benchmarking**: Systematic comparison of DCR against tree-based models (Random Forest, XGBoost, CatBoost) and deep learning models (NODE, TabNet)
- **Interpretability Assessment**: Evaluation of model explanations and logical rule quality
- **Tabular Data Focus**: Specialized evaluation for tabular datasets where interpretability is crucial
- **Credit Risk Application**: Real-world case study demonstrating practical utility in regulated environments
- **Reproducible Results**: Fixed random seeds and systematic hyperparameter optimization

## Project Structure

```
DCR-Evaluator/
├── data/                   # Dataset handling and preprocessing
├── models/                 # Model implementations and wrappers
├── evaluation/             # Metrics and interpretability assessment
├── benchmarks/             # Automated benchmarking pipeline
├── credit_risk/            # Credit risk scoring application
├── visualization/          # Results visualization and plotting
├── config/                 # Configuration files
├── tests/                  # Unit tests
├── notebooks/              # Jupyter notebooks for analysis
├── results/                # Experimental results and outputs
└── requirements.txt        # Python dependencies
```

## Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd DCR-Evaluator
```

2. Create and activate a virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # Linux/Mac
# venv\Scripts\activate   # Windows
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

## Quick Start

### Running Benchmarks

Execute the complete benchmarking suite:
```bash
python -m benchmarks.run_benchmarks
```

### Credit Risk Analysis

Run the credit risk scoring analysis:
```bash
python -m credit_risk.analyze
```

### Generate Reports

Create evaluation reports and visualizations:
```bash
python -m evaluation.generate_reports
```

## Models Evaluated

### Deep Concept Reasoning (DCR)
- Neural-symbolic approach generating logical rules from concept abstractions
- Provides both local and global explanations
- Maintains interpretability while achieving competitive accuracy

### Baseline Models
- **Tree-based**: Random Forest, XGBoost, CatBoost
- **Deep Learning**: NODE (Neural Oblivious Decision Ensembles), TabNet
- **Traditional**: Logistic Regression, Decision Trees

## Evaluation Metrics

### Performance Metrics
- Classification accuracy
- ROC AUC score
- Precision, Recall, F1-score
- Cross-validation consistency

### Interpretability Metrics
- Rule complexity and coverage
- Feature importance analysis
- Explanation stability
- Human comprehensibility assessment

## Datasets

The evaluation uses carefully selected tabular datasets that meet specific criteria:
- Real-world origin (not synthetic)
- Heterogeneous features from different sources
- Moderate dimensionality
- Well-documented with clear feature definitions
- Sufficient complexity (not trivially solvable)
- Balanced classes after preprocessing

## Configuration

Model hyperparameters and experimental settings can be configured through YAML files in the `config/` directory:
- `config/models.yaml`: Model-specific hyperparameters
- `config/datasets.yaml`: Dataset selection and preprocessing settings
- `config/evaluation.yaml`: Evaluation criteria and metrics

## Results

Results are automatically saved to the `results/` directory, including:
- Performance comparison tables
- Interpretability analysis reports
- Generated logical rules and explanations
- Visualization plots and figures

## Contributing

This project follows academic research standards:
- All code includes comprehensive documentation
- Experiments are reproducible with fixed random seeds
- Statistical significance testing for all comparisons
- Clear separation of concerns across modules

## License

This project is part of academic research at USI Lugano. Please contact the author for usage permissions.

## Citation

If you use this code in your research, please cite:

```bibtex
@mastersthesis{horn2025dcr,
  title={Tabular Deep Concept Reasoning},
  author={Horn, Marian},
  year={2025},
  school={Universita della Svizzera italiana},
  type={Master's thesis}
}
```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact

For questions or collaborations, please contact: marian.horn@usi.ch