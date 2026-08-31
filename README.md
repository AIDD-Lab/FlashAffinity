# FlashBind

[![Paper](https://img.shields.io/badge/Paper-MLSB%202025-blue)](https://openreview.net/pdf?id=TZTahjQNjX)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

Official implementation of **"FlashBind: Towards Accurate and Efficient Structure-based Virtual Screening"**, Accepted at **TMLR 2026**.

A ultra-fast protein-ligand affinity prediction framework supporting multiple prediction tasks: binary activity classification, enzyme-substrate interaction prediction, and affinity value regression.

## Environment Setup

```bash
conda env create -f env.yaml
conda activate flashaffinity
```

## Model & Data

- **Model Checkpoints**: [Model](https://huggingface.co/clorf6/FlashBind)
- **Datasets**: [Datasets](https://huggingface.co/datasets/clorf6/FlashBind)

## Supported Tasks

| Task | Description | Output |
|------|-------------|--------|
| `binary` | Binary activity classification | Activity probability (0-1) |
| `value` | Affinity value regression | log₁₀(IC50/Ki/Kd) value |
| `enzyme` | Enzyme-substrate interaction | Activity score (0-1) |

## Documentation

- [Training Guide](docs/train.md)
- [Prediction Guide](docs/predict.md)
- [Data Processing Guide](docs/data_process.md)
- [Evaluation Guide](docs/eval.md)

## Citation

```bibtex
@article{jiang2025flashbind,
  title={FlashBind: Towards Accurate and Efficient Structure-based Virtual Screening},
  author={Jiang, Songlin and Chen, Yifan and Krishnan, Aarti and Zhang, Yu and Jin, Wengong},
  journal={bioRxiv},
}
```

## Acknowledgments

We thank the [FABind+](https://github.com/QizhiPei/FABind) team and [Boltz-2](https://github.com/jwohlwend/boltz) team for their outstanding contributions to the community and for making their code openly available.
