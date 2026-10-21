Sentra Baby: Autonomous Infant Distress Recognition & Broadcast System

> An open-source, edge-AI-powered passive audio monitoring and multi-device broadcast framework designed to autonomously decode infant distress signals (hunger, pain, discomfort, and fatigue) in real-time. Developed by a Data Science MSc Graduate as part of an innovative Health-Tech portfolio for Global Talent recognition.

---

The Innovation & Market Gap
Traditional baby-monitoring solutions and existing open-source classifiers often suffer from a major UX flaw: **they require active user input**, such as a parent manually pressing a button to record or analyze a cry. 

**Sentra Baby** solves this gap by functioning as a **standalone, passive background application**. It continuously listens for acoustic triggers, processes the audio locally using deep learning, and instantly pushes multi-device alerts to parents or caregivers who may not be physically in the room.

---

System Architecture & Workflow

The end-to-end pipeline operates autonomously through four integrated layers:

[ Passive Ambient Audio Stream ] 
       │
       ▼
[ Automated Voice Activity Detection (VAD) & Resampling ] 
       │
       ▼
[ Feature Extraction & CNN Inference ] (Classifying Distress State: Hunger / Pain / Tired)
       │
       ▼
[ Multi-Device Broadcast Gateway ] (Instant push notification / cross-device alert to caregivers)

---

Core Technical Features

- Passive Ambient Monitoring: Operates continuously without manual recording triggers.
- Deep Learning Classification: Built using Convolutional Neural Networks (CNNs) trained on spectrogram representations of infant cries via Librosa and TensorFlow.
- Multi-Device Broadcast Engine: Designed to scale alerts across disparate endpoints (mobile, web, or IoT speakers) to ensure immediate notification.
- Edge-Ready Design: Optimized for low-latency inference suitable for local deployment.

---

Tech Stack

- Core Language: Python
- Deep Learning & Frameworks: TensorFlow / Keras
- Audio Signal Processing: Librosa
- Utilities: NumPy, Matplotlib

How to Test & Run Locally

Clone the repository:
git clone [https://github.com/ChineduDfx/sentra-baby-AI.git](https://github.com/ChineduDfx/sentra-baby-AI.git)
cd sentra-baby

Install dependencies:
pip install -r requirements.txt

Run autonomous pipeline simulation:
python app.py --mode passive
