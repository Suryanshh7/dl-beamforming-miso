# Deep Learning-Based Beamforming and Power Allocation in MISO Systems

## 1. Overview
This project investigates the application of deep learning techniques to optimize beamforming and power allocation in Multiple Input Single Output (MISO) wireless communication systems. The goal is to replace traditional optimization-based approaches with data-driven models that can efficiently learn optimal transmission strategies.

---

## 2. Objective
To design a neural network model that learns optimal beamforming weights and power allocation policies in order to:
1. Improve signal quality  
2. Enhance transmission efficiency  
3. Reduce computational complexity compared to traditional methods  

---

## 3. System Architecture

![MISO System](https://upload.wikimedia.org/wikipedia/commons/2/2b/MIMO_system_model.svg)

*Figure: Multiple transmit antennas sending signals to a single receiver through a wireless channel.*

---

## 4. Fundamental Concepts

### 4.1 What is MISO?
MISO (Multiple Input Single Output) systems use multiple transmitting antennas and a single receiving antenna.

This setup improves:
1. Signal strength  
2. Reliability  
3. Resistance to fading  

---

### 4.2 What is Beamforming?

![Beamforming](https://upload.wikimedia.org/wikipedia/commons/3/3b/Beamforming_illustration.png)

Beamforming is a signal processing technique that directs transmission energy toward a specific receiver instead of spreading it uniformly.

It works by:
1. Adjusting phase and amplitude of transmitted signals  
2. Creating constructive interference at the receiver  

👉 Intuition: Focus energy where it is needed instead of wasting it in all directions.

---

### 4.3 What is Power Allocation?

![Power Allocation](https://upload.wikimedia.org/wikipedia/commons/5/5a/Water_filling_algorithm.svg)

Power allocation determines how transmission power is distributed across antennas or channels.

Goals:
1. Maximize signal-to-noise ratio (SNR)  
2. Reduce interference  
3. Improve energy efficiency  

---

### 4.4 What is a Communication Channel?

![Wireless Channel](https://upload.wikimedia.org/wikipedia/commons/8/8c/Multipath_propagation.svg)

The channel represents how signals propagate from transmitter to receiver and includes:
1. Noise  
2. Interference  
3. Fading effects  

👉 The channel is dynamic and unpredictable, making optimization challenging.

---

### 4.5 Why Use Deep Learning?
Traditional beamforming relies on solving complex optimization problems repeatedly.

Deep learning offers:
1. Fast inference after training  
2. Ability to learn non-linear relationships  
3. Reduced computational overhead  

---

### 4.6 Role of Neural Network

The neural network learns a mapping:

**Input:**
- Channel state information  

**Output:**
- Beamforming weights  
- Power allocation values  

👉 Instead of solving optimization equations each time, the model directly predicts optimal configurations.

---

## 5. Mathematical Formulation

### 5.1 Signal Model

The received signal is:

\[
y = \mathbf{h}^H \mathbf{w} x + n
\]

Where:
- \( \mathbf{h} \): Channel vector  
- \( \mathbf{w} \): Beamforming weights  
- \( x \): Transmitted signal  
- \( n \): Noise  

---

### 5.2 Signal-to-Noise Ratio (SNR)

\[
\text{SNR} = \frac{|\mathbf{h}^H \mathbf{w}|^2}{\sigma^2}
\]

👉 Goal: Maximize signal strength relative to noise.

---

### 5.3 Power Constraint

\[
||\mathbf{w}||^2 \leq P
\]

👉 Ensures total transmit power is limited.

---

### 5.4 Optimization Problem

\[
\max_{\mathbf{w}} \; |\mathbf{h}^H \mathbf{w}|^2
\]

subject to:

\[
||\mathbf{w}||^2 \leq P
\]

👉 Traditional methods solve this repeatedly (computationally expensive).

---

### 5.5 Deep Learning Approach

\[
\mathbf{w} = f_\theta(\mathbf{h})
\]

Where:
- \( f_\theta \): Neural network  
- Input: Channel information  
- Output: Optimal beamforming weights  

👉 Model learns mapping instead of solving optimization each time.

---

## 6. Methodology

1. Generated simulation-based dataset representing channel conditions  
2. Designed a neural network model to learn optimal transmission strategies  
3. Trained the model using supervised learning  
4. Evaluated performance against traditional methods  

---

## 7. Performance Metrics

Model performance is evaluated using:

1. Signal-to-Noise Ratio (SNR)  
2. Throughput/Data Rate  
3. Power Efficiency  

---

## 8. Results

1. Achieved efficient beamforming strategies using learned models  
2. Demonstrated improved signal optimization compared to baseline approaches  
3. Reduced computational complexity for real-time applications  

---

## 9. Key Insights

1. Deep learning can approximate complex optimization problems effectively  
2. Data-driven approaches adapt better to varying channel conditions  
3. Performance depends heavily on quality of training data  

---

## 10. Applications

1. 5G / 6G wireless communication systems  
2. Massive MIMO systems  
3. Smart antenna systems  
4. Wireless resource allocation  

---

## 11. Future Work

1. Extend to MIMO systems  
2. Use reinforcement learning for adaptive optimization  
3. Real-time deployment  
4. Hybrid model-based + ML approaches  

---

## 12. Author
Suryansh
