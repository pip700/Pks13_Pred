

# Pks13\_Pred

**AttentiveFP-based classification model for Pks13 (Mycobacterium tuberculosis)**

---

## 📚 Table of Contents

* [Features](#-features)
* [Installation](#-installation)
* [Usage](#-usage)
* [Output](#-output)
* [Troubleshooting](#-troubleshooting)
* [Contributors](#-contributors)
* [Citation](#-citation)

---

## 🚀 Features

* ✅ Predicts whether a molecule is a **Blocker** or **Non-blocker**
* 🐳 Easy-to-use **Docker container** (no manual dependency installation)
* ⚙️ Runs on **CPU**
* 🔍 Provides **atom- and bond-level importance scores**
* 💾 Saves results in **timestamped directories**
* 🖼️ Generates visualization plots for model interpretation

---

## 📦 Installation

### 1. Install Docker

#### Windows (via WSL)

```powershell
wsl --install
sudo apt-get update
sudo apt-get install docker.io -y
```

#### Linux

```bash
sudo apt-get update
sudo apt-get install docker.io -y
```

📦 **Dependencies**: Already included in the Docker image.

---

## 🧪 Usage

### 1. Run the Docker container

```bash
sudo docker run -it --rm -v ${PWD}:/workspace ghcr.io/pip700/pks13_pred
```

### 2. Provide input

Inside the container:

* **Option 1**: Enter SMILES string directly

  ```
  COC1=CC=C(C=C1)CCN2CCC(CC2)NC3=NC4=CC=CC=C4N3CC5=CC=C(C=C5)F
  ```

* **Option 2**: Provide a CSV file containing a column of SMILES strings

  ```
  samples.csv
  ```

---

## 📤 Output

Results are saved in a **timestamped directory** in your working folder.

Includes:

* `Prediction.csv` → Predicted labels & probabilities
* `Atom-level_importance.csv` → Atom importance scores
* `Bond-level_importance.csv` → Bond importance scores
* `Atom_Bond-level.png` → Visualization of importance

---

## 🛠️ Troubleshooting

* **Docker not found** → Install Docker and add to PATH
* **Permission denied** → Run Docker with `sudo`
* **GPU not detected** → Currently supports **CPU only**

---

## 👥 Contributors

* [pip700](https://github.com/pip700)

---

## 📑 Citation

If you use **Pks13_Pred** in your research, please cite:

```bibtex
@article{pks13pred2025,
  author    = {Vineet, Dhairiya Agarwal, and Prabha Garg},
  title     = {Pks13_Pred: An AttentiveFP-based classification model for Pks13 inhibitors in Mycobacterium tuberculosis},
  journal   = {...},
  volume    = {...},
  year      = {2025},
  url       = {https://pubmed.ncbi.nlm.nih.gov/...},
  doi       = {...}
}
```

