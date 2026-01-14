# Analysis of Noise Effects in Chest X-ray Images Using Quantum Fourier Transform

## 📄 Project Overview

This project investigates the impact of different noise models (Gaussian and Salt-and-Pepper) on **Chest X-ray images** using **Quantum Computing** techniques. Specifically, it compares the frequency domain representations obtained via the **Quantum Fourier Transform (QFT)** against the classical Fast Fourier Transform (FFT).

The study demonstrates how quantum algorithms can allow for noise analysis in medical imaging by encoding image data into quantum states and analyzing spectral leakage.

## 🎯 Objectives

* **Image Preprocessing:** Extracting and normalizing 4x4 pixel patches from grayscale chest X-rays.
* **Noise Simulation:** Applying controlled **Gaussian Noise** (additive) and **Salt-and-Pepper Noise** (impulsive).
* **Quantum Encoding:** Mapping image intensity values to quantum states using **Amplitude Encoding**.
* **Spectral Analysis:** Implementing a 4-qubit QFT circuit to analyze frequency distributions.
* 
**Benchmarking:** Validating quantum results against classical 1D FFT.



## 🛠️ Tech Stack & Dependencies

The project is implemented in Python using the following libraries:

* **Qiskit:** For quantum circuit construction and execution.
* **Qiskit Aer:** For local quantum simulation (`aer_simulator`).
* **NumPy:** For classical matrix operations and FFT benchmarking.
* **Matplotlib:** For visualizing histograms and frequency spectra.
* **Pillow (PIL):** For image loading and processing.

## 🚀 Methodology

1. **Data Preparation:** A 4x4 patch is extracted from a larger Chest X-ray to suit a 4-qubit system ( pixels).
2. **State Preparation:** The flattened, normalized pixel vector is initialized onto the quantum circuit.
3. **QFT Implementation:** A standard QFT circuit is applied using Hadamard and Controlled-Phase rotation gates.
4. **Measurement:** The circuit is executed with **10,000 shots** to generate a probability distribution of frequency states.
5. **Comparison:** The results are compared with classical `np.fft.fft` squared magnitudes.

## 📊 Key Results

* **Clean & Gaussian Noisy Images:** Both show energy concentrated in low-frequency states (e.g., ), indicating smooth spatial structures. Gaussian noise causes only minor high-frequency leakage.


* 
**Salt-and-Pepper Noise:** Shows significant energy redistribution across mid- and high-frequency states (e.g., , ), accurately detected by the QFT.


* 
**Validation:** The QFT measurement probabilities closely align with classical FFT results, proving the correctness of the quantum implementation.



## 💻 Installation & Usage

1. **Clone the repository:**
```bash
git clone https://github.com/SatyaKrishna2811/Your-Repo-Name.git
cd Your-Repo-Name

```


2. **Install dependencies:**
```bash
pip install numpy matplotlib qiskit qiskit-aer pillow

```


3. **Run the analysis:**
```bash
python main.py

```


*(Note: Ensure you have a sample X-ray image in the path or update the image path in the script).*

## 👥 Contributors
This project was developed as part of the Principal of Quantum Information Processing (PQIP) course at Amrita Vishwa Vidyapeetham.

Vepuri Satya Krishna (DL.AI.U4AID24140)

Gowripriya R (DL.AI.U4AID24113)

Yaalini R (DL.AI.U4AID24043)
* **Vepuri Satya Krishna** (DL.AI.U4AID24140)
* **Gowripriya R** (DL.AI.U4AID24113)
* **Yaalini R** (DL.AI.U4AID24043)

**Supervisor:** Prof. Dr. Mrittunjoy Guha Majumdar

## 📜 License

This project is created for academic purposes as part of the B.Tech AI & DS curriculum.
This project is for educational and research purposes only and should not be used as a primary diagnostic tool without clinical validation.

---
