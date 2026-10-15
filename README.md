<!--
  PhytoDetect AI / GrapeCare
  README refreshed to document the features and technologies currently visible in this repository.
-->

<div align="center">

# 🍇 PhytoDetect AI
### GrapeCare — AI-Powered Grape Leaf Disease Screening

An image-based grape leaf screening web application built with Flask and TensorFlow/Keras. Upload a leaf image to receive a predicted class and confidence scores in a simple, farmer-friendly interface.

[**🌐 Open the Hosted Demo**](https://huggingface.co/spaces/gagangowda08/grape) · [**📂 View Source Code**](https://github.com/gaganngowdaa08/PhytoDetect-AI)

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![License](https://img.shields.io/badge/License-Not%20Specified-lightgrey?style=for-the-badge)

</div>

---

## 📌 Overview

GrapeCare is designed to make preliminary grape leaf disease screening more accessible. A user uploads a leaf image, the Flask backend preprocesses it, and a saved TensorFlow/Keras model predicts the most likely class. Results include confidence values for the leading predictions, helping users review the model output.

> **Important:** This is an AI-assisted screening project, not a substitute for advice from an agricultural expert. Predictions depend on image quality and the model's training data.

## ✨ Features

- **Image-based prediction** — Upload a grape leaf image through the web interface.
- **Four configured prediction classes** — Black Rot, Esca, Healthy, and Leaf Blight.
- **Top prediction and runner-up** — The backend returns the two highest-scoring classes with their confidence values.
- **Visual results** — Chart.js is included in the interface to present results visually.
- **Multilingual interface** — Language resources are provided for English, Hindi, and Kannada.
- **Personalized appearance** — Includes selectable color themes and a dark-mode option.
- **Chat assistant integration** — The interface loads an embedded Botpress web chat.
- **Simple web stack** — Flask serves the application and connects the browser interface to the saved model.

## 🧭 How It Works

1. **Upload:** The user selects a grape leaf image.
2. **Preprocess:** The backend resizes the image to 224 × 224 pixels and normalizes pixel values.
3. **Predict:** The saved Keras model generates class scores.
4. **Present:** The application returns the top two predictions and their confidence values for display.

## 🧪 Supported Predictions

| Model label | Display meaning |
|---|---|
| `black_rot` | Black Rot |
| `esca` | Esca |
| `healthy` | Healthy leaf |
| `leaf_blight` | Leaf Blight |

The class list above reflects the current `CLASS_NAMES` configuration in `app.py`. Model accuracy and dataset size should only be reported alongside verified evaluation results.

## 🛠️ Technology Stack

| Layer | Technologies |
|---|---|
| Backend | Python, Flask |
| Machine learning | TensorFlow/Keras |
| Image processing | Pillow, NumPy |
| Frontend | HTML, CSS, JavaScript |
| Data visualization | Chart.js |
| Chat integration | Botpress web chat |
| Production server dependency | Gunicorn |

## 📁 Repository Structure

```text
PhytoDetect-AI/
├── app.py                  # Flask routes and prediction logic
├── index.html              # Web interface
├── grapecare_model.keras   # Saved Keras model
├── requirements.txt        # Python dependencies
├── en.json                 # English language resources
├── hi.json                 # Hindi language resources
├── kn.json                 # Kannada language resources
├── bot_knowledge.txt       # Chat assistant knowledge content
├── Procfile.txt            # Gunicorn launch configuration
└── README.md
```

## 🚀 Run Locally

### 1. Clone the repository

```bash
git clone https://github.com/gaganngowdaa08/PhytoDetect-AI.git
cd PhytoDetect-AI
```

### 2. Create and activate a virtual environment

**Windows (PowerShell)**

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

**macOS / Linux**

```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 3. Install the dependencies

```bash
python -m pip install --upgrade pip
pip install -r requirements.txt
```

### 4. Check the Flask template location

Flask's `render_template("index.html")` looks for the HTML file in a `templates/` directory. In this repository, `index.html` is currently at the project root. Before starting the application, place a copy in the expected location:

**Windows (PowerShell)**

```powershell
New-Item -ItemType Directory -Force templates
Copy-Item index.html templates/index.html
```

**macOS / Linux**

```bash
mkdir -p templates
cp index.html templates/index.html
```

### 5. Start the Flask server

```bash
python app.py
```

Open [http://127.0.0.1:5000](http://127.0.0.1:5000) in your browser.

## ☁️ Hosted Demo

The project README previously listed this Hugging Face Space as the hosted demo:

**[GrapeCare on Hugging Face Spaces](https://huggingface.co/spaces/gagangowda08/grape)**

Availability can depend on the hosting service and its current configuration.

## 👨‍💻 Author

**Gagan Gowda B G**

- GitHub: [@gaganngowdaa08](https://github.com/gaganngowdaa08)
- LinkedIn: [Gagan Gowda B G](https://www.linkedin.com/in/gagan-gowda-b-g-1b63a22b4/)

---

<div align="center">

Built to explore practical applications of deep learning for agricultural support. 🍃

</div>
