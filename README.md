# Knowledge Distillation for Safety-Critical Applications

<p align="center">
<img alt="Python" src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge" />
  <img alt="PyTorch" src="https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge" />
  <img alt="Machine Learning" src="https://img.shields.io/badge/Machine%20Learning-102230?style=for-the-badge" />
  <img alt="Data Science" src="https://img.shields.io/badge/Data%20Science-1F77B4?style=for-the-badge" />
</p>

<p align="center">
  <strong>A compact-model training and evaluation workflow for studying robustness, calibration, and distribution-shift behavior.</strong>
</p>

This project explores how student models can learn from larger teachers while preserving reliability under challenging conditions. It focuses on adversarial robustness, calibration quality, and performance under distribution shifts.

## Core Capabilities

- Implements knowledge-distillation evaluation workflows.
- Assesses adversarial robustness using attack-style perturbation tests.
- Evaluates calibration and uncertainty behavior.
- Frames compact-model performance for safety-sensitive contexts.

## Technical Architecture

The repository includes a primary evaluation script and documentation describing the project objectives, metrics, and experimental workflow. It is intentionally compact for focused experimentation.

## Architecture Diagram

```mermaid
%%{init: {"flowchart": {"nodeSpacing": 55, "rankSpacing": 70, "curve": "basis"}, "themeVariables": {"fontSize": "16px", "fontFamily": "Inter, ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, Segoe UI, sans-serif"}}}%%
flowchart TD
  Teacher["Teacher Model Outputs"] --> Distill["Knowledge Distillation"]
  Data["Evaluation Data"] --> Student["Student Model"]
  Distill --> Student
  Student --> Robustness["Adversarial Robustness Tests"]
  Student --> Calibration["Calibration Metrics"]
  Student --> Shift["Distribution Shift<br/>Evaluation"]
  Robustness --> Report["Safety Evaluation Summary"]
  Calibration --> Report
  Shift --> Report

  classDef inputs fill:#E0F2FE,stroke:#0284C7,color:#0C4A6E,stroke-width:2.5px;
  classDef process fill:#EDE9FE,stroke:#7C3AED,color:#4C1D95,stroke-width:2.5px;
  classDef data fill:#CCFBF1,stroke:#0D9488,color:#134E4A,stroke-width:2.5px;
  classDef agent fill:#FCE7F3,stroke:#DB2777,color:#831843,stroke-width:2.5px;
  classDef output fill:#FEF9C3,stroke:#CA8A04,color:#713F12,stroke-width:2.5px;
  class Teacher,Data inputs;
  class Student,Robustness,Calibration,Shift process;
  class Distill agent;
  class Report output;
  linkStyle default stroke:#475569,stroke-width:2.5px;
```

## Technology Stack

- Python for experiment execution.
- PyTorch-oriented model evaluation workflow.
- Robustness and calibration metrics.
- Notebook/script-ready structure for future experiment expansion.

## Repository Structure

- `evaluation.py` - Evaluation workflow.
- `LICENSE` - Repository license.
- `README.md` - Project documentation.

## Getting Started

```bash
python -m venv .venv
source .venv/bin/activate
pip install torch numpy scikit-learn matplotlib
```

```bash
python evaluation.py
```

## Professional Context

This project demonstrates model-compression research awareness, safety-oriented evaluation, and disciplined ML experiment framing.
