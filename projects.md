---
name: Shrinisha Nirmalkumar
title: Projects - Shrinisha 
---


## End-to-End Encrypted Messaging with Telegram MTProto 2.0
**Software/Platforms:** Python 3.10+, PyQt6 GUI  
**Crypto Stack:** Diffie–Hellman (key exchange), AES-CBC (confidentiality), SHA-256 (integrity)  
**Networking:** TCP sockets • **Logging:** terminal + JSON • **Architecture:** P2P clients (Initiator/Listener) + lightweight coordination server with offline queue

- Implemented client-side E2EE: peers derive a shared secret via Diffie–Hellman, then derive AES session keys/IVs; the server never sees plaintext. Includes identity handshake and session-scoped keys/salts for forward secrecy.
- Ensured reliable delivery: encrypted offline message queuing on the server, automatic reconnection, peer online/offline detection, and typing indicators for smooth real-time chat.
- Built a usable desktop app: PyQt6 chat window (login, history, status badges), structured JSON logs per action with secure cleanup at session end; clear module split.
- Integrity & privacy guarantees: SHA-256–derived message keys protect integrity; session-specific materials and ephemeral keys for queued messages preserve confidentiality vs. cloud-chat designs.

---

## Testing Biases and Fairness Against Different Models: A Comparative Study
**Software/Platforms:** Python; LoRA fine-tuning on Google Colab/Kaggle T4 GPUs (~15 GB VRAM)  
**Data:** CrowS-Pairs (stereotype vs. anti-stereotype across gender, race, religion, age)  
**Models:** Qwen1.5-1.8B-Chat, TinyLLaMA-1.1B-Chat, Phi-1.5

- Ran baseline bias tests on CrowS-Pairs and recorded preference rates for stereotypical sentences to quantify bias across identity axes.
- Applied lightweight debiasing via LoRA (4-bit quantization, small batches) using anti-stereotypical examples; re-evaluated on generalized and bias-type-filtered subsets.
- **Key results**  Generalized set: Qwen 58%→52% (↓6 pts), TinyLLaMA 51%→59% (↑8 pts, worsened), Phi-1.5 58.7%→57.4% (↓1.3 pts).Bias-type-specific: Qwen 47.06%→43.89% (↓3.17), TinyLLaMA 52.94%→46.00% (↓6.94), Phi-1.5 61.48%→60.31% (↓1.17).
- **Takeaway:** Targeted (bias-type-specific) fine-tuning consistently reduces bias, especially for smaller, less pre-aligned models, while untargeted, generalized debiasing can be ineffective or counterproductive.

---

## CHURNINSIGHT AI: Predictive Analytics for Customer Retention
**Software Requirements:** Python, Scikit-learn, Matplotlib

- Developed a predictive model to identify high-risk banking clients, reducing churn by **20%** and improving retention by **15%**.
- Incorporated methods like Random Forests; improved attrition-prediction accuracy by **15%** via detailed behavior analysis.
- Utilized customer demographic & transactional data to drive proactive retention strategies, improving loyalty across **10,000+** data points.

---

## RACE PULSE: Predicting Marathon Times with Data Power
**Software Requirements:** Python, Scikit-learn, Matplotlib  
**Data Sources:** Boston, Chicago, New York, London, and Berlin Marathon datasets

- Built a machine-learning model to predict marathon finish times, achieving **R² = 0.95** with Random Forests outperforming traditional methods by **~15%**.
- Integrated factors like weather conditions, pacing strategies, and runner demographics, yielding actionable insights for optimizing athlete sponsorship and training.

---

## An Improved Driver Safety Mechanism Using IoT
**Software:** Python, OpenCV  
**Hardware:** Arduino, LDR sensor, RF transmitters

- Designed detection for alcohol levels over **0.02% BAC**, increasing detection accuracy by **25%** and improving safety measures.
- Integrated signboard detection, drowsiness detection with alerts, and accident notifications to authorities resulting in a **30%** reduction in driver response time and enhanced road safety for **5,000+** users.
