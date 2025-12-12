# **Multi-Agent LLM Council for Clinical Reasoning Using 4-Bit Quantized Models**

## Overview  
This repository implements a **multi-agent LLM council architecture** for clinical reasoning tasks.  
Multiple lightweight **4-bit quantized language models** independently analyze a patient case, and a separate **chairman model** synthesizes their outputs into a final, higher-quality answer.

The goal is to showcase how **ensemble reasoning**, **quantized inference**, and **structured prompt orchestration** can:  
- Improve reasoning stability  
- Reduce hallucinations  
- Increase transparency  
- while still being GPU-efficient.

> **Disclaimer:**  
> This project is intended **strictly for research and educational purposes**.  
> It must **not** be used for real medical diagnosis or clinical decision-making.

---

## Key Features  
- **Multi-agent LLM council** (3 member models + 1 chairman).  
- **4-bit quantized inference** using `bitsandbytes` for low VRAM usage.  
- Automatic model loading via HuggingFace Hub.  
- Structured reasoning prompts for:
  - Differential diagnosis  
  - Initial investigations  
  - Step-by-step reasoning  
  - Concise summary  
- Chairman performs:
  - Cross-member consistency check  
  - Error/hallucination detection  
  - Reasoning quality ranking  
  - Final synthesized decision  

---

## Repository Structure  
```bash
.
├── app.py           # Core council implementation
├── requirements.txt     # Dependencies
└── README.md            # Project documentation

