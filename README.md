# Plant Disease Recognition Using Deep Learning

This repository implements a deep learning-based plant disease recognition system using Convolutional Neural Networks (CNNs) and transfer learning with MobileNetV2.

## Project Structure

```
├── cimp.ipynb           # Main Jupyter Notebook (data prep, model training, evaluation, and inference)
├── class_names.json     # JSON file containing the list of 41 plant disease classes
├── cells.txt            # Project reference notes and code snippets
├── .gitignore           # Ignores large datasets, virtual envs, and heavyweight models
└── README.md            # This project guide
```

---

## Getting Started

To run this project locally, follow these steps:

### 1. Prerequisites & Environment Setup
The project uses a Python virtual environment to manage dependencies. Specifically, it is configured for hardware-accelerated deep learning on Windows using **TensorFlow DirectML**.

Create and activate a Python virtual environment (Python 3.10 is recommended):
```bash
# Create virtual environment
python -m venv .venv310

# Activate virtual environment (Windows PowerShell)
.\.venv310\Scripts\Activate.ps1

# Or Windows Command Prompt
.\.venv310\Scripts\activate.bat
```

### 2. Install Dependencies
Install TensorFlow with DirectML support and required libraries:
```bash
pip install tensorflow-cpu==2.10.0 tensorflow-directml-plugin "protobuf<3.20,>=3.19.6" "numpy<2.0.0" "keras<2.11,>=2.10.0" ipykernel
```

Register the virtual environment kernel to Jupyter Notebook:
```bash
python -m ipykernel install --user --name=venv310 --display-name "Python 3.10 (.venv310)"
```

### 3. Add the Dataset
Due to GitHub repository limits, the `dataset/` directory (containing ~8,581 images across 41 classes, total size ~47GB) is **ignored** by Git.
* Ask project owners/collaborators for access to the dataset zip/folder.
* Place the dataset directory directly in the project root under the folder name `dataset/`.
* Your directory layout should look like this:
  ```
  Final Year Project/
  ├── dataset/
  │   ├── Ashok.H/
  │   ├── Ashok.U/
  │   └── ... (41 classes)
  ```

---

## Collaboration Guide (For Project Mates)

If you are a collaborator on this project:

1. **Clone the repository**:
   ```bash
   git clone <your-repository-url>
   cd "Final Year Project"
   ```
2. Set up the Python virtual environment and download the dataset as shown in the [Getting Started](#getting-started) section.
3. Keep the large `.keras` model files and the `dataset/` directory ignored to avoid hitting GitHub upload size limits.
4. When writing code or making modifications, work in branches and open pull requests for team reviews.
