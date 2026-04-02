<div align="center">

# Worker Sentry

### Real-Time PPE Compliance Detection Powered by AI

[![Python](https://img.shields.io/badge/Python-3.8%2B-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![YOLO](https://img.shields.io/badge/YOLO-Fine--Tuned-FF6B35?style=for-the-badge)](https://ultralytics.com)
[![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)](https://pytorch.org)
[![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white)](https://opencv.org)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)](LICENSE)

> **SafeVision AI** — Automatically detect PPE violations in workplace video footage. Protect your workforce before incidents happen.

</div>

---

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Model Details](#model-details)
- [Getting Started](#getting-started)
- [Project Structure](#project-structure)
- [Usage](#usage)
- [Output & Results](#output--results)
- [Contributing](#contributing)
- [License](#license)

---

## Overview

**Worker Sentry** is a real-time AI-powered safety monitoring system that automatically detects PPE (Personal Protective Equipment) compliance in workplace environments. Built on a fine-tuned YOLO model, it processes CCTV or pre-recorded video footage and flags workers who are not wearing required safety gear — helping organizations stay compliant and keep workers safe.

| Detection Target | Status |
|---|---|
| Hard Hat / Helmet | Supported |
| Safety Gloves | Supported |
| Safety Vest | Supported |
| Safety Goggles | Coming Soon |

---

## Features

- **Real-Time Detection** — Frame-by-frame inference on `.mp4` video files
- **High Accuracy** — Fine-tuned YOLO model trained specifically on PPE datasets
- **Compliance Reports** — Automatic summaries of violations per video
- **Violation Alerts** — Flagged timestamps for non-compliant frames
- **Jupyter Notebook Interface** — Easy-to-use interactive workflow
- **Configurable Thresholds** — Adjust detection confidence per use case

---

## Model Details

| Property | Detail |
|---|---|
| **Architecture** | YOLO (You Only Look Once) |
| **Training** | Fine-tuned on PPE detection dataset |
| **Detection Classes** | Helmets, Gloves, Safety Vests |
| **Frameworks** | Python, OpenCV, PyTorch |
| **Input** | `.mp4` video files |
| **Output** | Annotated video + compliance report |

---

## Getting Started

### Prerequisites

Ensure you have the following installed:

- Python 3.8 or higher
- `pip` package manager
- CUDA-compatible GPU *(recommended for real-time performance)*

### Installation

**1. Clone the repository:**

```bash
git clone https://github.com/your-username/safevision-ai.git
cd Worker-Sentry
```

**2. Install dependencies:**

```bash
pip install -r requirements.txt
```

**3. Add your video files:**

Place your `.mp4` footage into the `Videos/` directory:

```bash
cp /path/to/your/footage.mp4 Videos/
```

**4. Launch the notebook:**

```bash
jupyter notebook WorkerSentry.ipynb
```

---

## Project Structure

```
Worker-Sentry/
│
├── Videos/                  # Place your .mp4 files here
├── Output/                  # Annotated videos & reports saved here
│
├── main.ipynb       # Main Jupyter Notebook
├── ppe.pt          # Fine-tuned YOLO weights
│
│
├── requirements.txt         # Python dependencies
├── LICENSE
└── README.md
```

---

## Usage

1. Open `WorkerSentry.ipynb` in Jupyter
2. Set the path to your video file in the configuration cell
3. Adjust confidence thresholds if needed (default: `0.5`)
4. Run all cells — detections and reports will be saved to `Output/`

```python
# Example configuration
VIDEO_PATH = "Videos/construction_site.mp4"
CONFIDENCE_THRESHOLD = 0.5
SAVE_OUTPUT = True
```

---

## Output & Results

After running the notebook, you will find in the `Output/` folder:

- **Annotated Video** — Original footage with bounding boxes highlighting detected PPE and violations
- **Compliance Report** — A summary including:
  - Total frames analyzed
  - Number of violation frames
  - Per-worker compliance rate
  - Timestamped violation log

---

## Contributing

Contributions are welcome! To get started:

1. Fork this repository
2. Create a feature branch: `git checkout -b feature/your-feature`
3. Commit your changes: `git commit -m 'Add your feature'`
4. Push to the branch: `git push origin feature/your-feature`
5. Open a Pull Request

Please read [CONTRIBUTING.md](CONTRIBUTING.md) before submitting changes.

---

## License

This project is licensed under the MIT License.

---

<div align="center">

Built for workplace safety

</div>
