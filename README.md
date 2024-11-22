Welcome to the repository for the Personalized Chatbot with Dynamic Responses project! This document outlines the project structure, objectives, methodologies, and features. This chatbot is a multilingual medical assistant developed as part of the Graduation Project for the Generative AI Professional Track.
Project Overview

This project aims to address the challenges in accessing real-time, accurate medical information across multiple languages. Built using state-of-the-art machine learning techniques, the chatbot provides medical term disambiguation, multilingual support, and real-time responses to assist patients, healthcare professionals, and students.
Key Features:

    Multilingual Medical Support: Handles queries in English, Arabic, and Spanish.
    Medical Abbreviation Disambiguation: Clarifies complex abbreviations with detailed explanations.
    Efficient Model Optimization: Utilizes Low-Rank Adaptation (LoRA) and 4-bit quantization for fast inference on low-resource devices.
    User-Friendly Interface: Built with Streamlit for seamless interaction.

Technologies Used
Languages:

    Python

Frameworks:

    Hugging Face Transformers: Model fine-tuning and inference.
    Streamlit: Front-end interface for user interaction.
    PyTorch: Model training and inference.

Supporting Tools:

    MeDAL Dataset: Medical Dataset for Abbreviation Disambiguation.
    LoRA: Memory-efficient model optimization.
    Unsloth: Fine-tuning framework.

Installation and Usage
Prerequisites:

    Python 3.8+
    GPU with CUDA support (recommended for inference)
    Required Python libraries: transformers, streamlit, torch, datasets.

Installation:

    Clone the repository:

git clone <repository_url>

Navigate to the project directory:

cd personalized-medical-chatbot

Install dependencies:

    pip install -r requirements.txt

Running the Chatbot:

    Start the Streamlit interface:

    streamlit run app.py

    Open the provided local URL in your browser.
    Interact with the chatbot by inputting medical queries.

Project Workflow

    Data Collection: Using the MeDAL dataset.
    Preprocessing: Tokenization and augmentation for model compatibility.
    Model Fine-Tuning: Gemma-7B optimized using LoRA.
    Testing: Ensuring accuracy, responsiveness, and multilingual support.

Key Metrics

    Training Time: ~10.57 minutes
    Memory Usage:
        Peak: 6.273 GB
        During training: 1.773 GB (~12% of system memory)
    Accuracy: High precision on multilingual medical terminology queries.

Challenges and Solutions

    Dataset Size: Managed using efficient loaders like Unsloth.
    Memory Constraints: Overcome with gradient checkpointing and quantization.
    Real-Time Performance: Achieved with LoRA optimization and prompt engineering.

Future Enhancements

    Expand language support to include additional regional languages.
    Integrate with live medical APIs for real-time updates.
    Develop mobile-friendly versions for broader accessibility.
