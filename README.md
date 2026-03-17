# 📊 Financial Sentiment Analysis System

An end-to-end MLOps ecosystem designed to perform **Financial Sentiment Analysis** using **Knowledge Distillation**. This system compresses the knowledge of a heavy Transformer (FinBERT) into a lightweight, high-performance **Bi-LSTM** model, optimized for real-time financial text processing.
## 🛰️ System Architecture

This project is organized into specialized repositories, linked here as **Git Submodules** to maintain a clean separation of concerns:

| Component | Description | Tech Stack | Repository |
|-----------|-------------|------------|------------|
| **AI Training** | Data generation via distillation, Bi-LSTM training, and experiment tracking. | Python, TensorFlow, MLflow, DVC | [Explore](https://github.com/alvaro-frank/sentiment_analysis) |
| **Backend API** | High-performance inference service using Clean Architecture. | FastAPI, MLflow, Pytest | [Explore](https://github.com/alvaro-frank/sentiment-analysis-backend) |
| **Frontend UI** | *[Planned]* Interactive visualization dashboard. | React, Three.js, TS | [TBD] |

## 🛠️ Key Features
- **Knowledge Distillation**: Uses a "Teacher-Student" strategy to transfer sentiment logic from FinBERT to a faster Bi-LSTM.
- **Clean Architecture**: The backend service decouples core business rules from technical infrastructure, following the same robust patterns used in 3D-BPP.
- **Production-Ready Inference**: Models are served using MLflow PyFunc wrappers, encapsulating preprocessing and model weights into a single portable artifact.
- **Automated Quality**: Integrated CI/CD pipelines for automated unit/integration testing and Docker image builds.
- **Financial Preprocessing**: Custom NLP pipeline that normalizes numbers and preserves critical negations (e.g., "not", "no") often lost in standard cleaning.

## ⚡ Quick Start

To run the current stable version of the backend service:

1. **Clone the Master Repository with Submodules**:
```bash
git clone --recursive https://github.com/alvaro-frank/sentiment-analysis-system.git
cd sentiment-analysis-system
```

2. **Launch via Docker Compose**:
```bash
docker-compose up --build
```

3. **Access API Documentation**:

Visit `http://localhost:8000/docs` to test the endpoints.

Developed by Álvaro Franco - [LinkedIn](https://www.linkedin.com/in/alvaro-jose-franco/) | [GitHub](https://github.com/alvaro-frank)
