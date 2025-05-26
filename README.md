# 🧠 Spikernary  
## On Using Ternary Neurons to Improve Performance of Spike-based Deep Q-Learning

This repository benchmarks the performance of **SNNs in Q-Learning** using three types of spiking neurons:

- **Binary spiking neurons** (DSQN)  
- **Symmetric ternary spiking neurons** (DTSQN)  
- **Asymmetric ternary spiking neurons** (DATSQN)  

These models are trained and evaluated on **Atari games** using the **Gymnasium** framework.

---

## 📦 Installation

Install the required Python dependencies:

```bash
pip install gymnasium
pip install stable-baselines3
pip install ale_py
pip install snntorch
pip install msgpack-numpy
pip install tensorboard
```

---

## 🚀 Usage

### 🧠 Training Agents

Run the corresponding script to train each agent:

```bash
python DATSQN_train.py    # Asymmetric ternary neurons
python DTSQN_train.py     # Symmetric ternary neurons
python DSQN_train.py      # Binary neurons
```

### 📊 Monitor Training with TensorBoard

```bash
tensorboard --logdir logs/
```

---

## 🧪 Testing Trained Models

Run the relevant test script after training:

```bash
python DATSQN_test.py
python DTSQN_test.py
python DSQN_test.py
```

### 👀 Watch the Agent Play

To render the environment and visualize gameplay:

1. Open the appropriate test script.
2. Uncomment the `env.render()` line in the main test loop:
   - `DATSQN_test.py`: Line **248**
   - `DTSQN_test.py`: Line **238**
   - `DSQN_test.py`: Line **235**

### ⚠️ Environment Consistency

Ensure the environment ID (e.g., `'Breakout'`) is **the same** in both training and testing to avoid errors.

---

## 📈 View Testing Results

You can use TensorBoard to view evaluation metrics:

```bash
tensorboard --logdir logs/
```

---

## 📁 Project Structure

```
├── DATSQN_train.py        # Train using asymmetric ternary neurons
├── DATSQN_test.py         # Test DATSQN model
├── DTSQN_train.py         # Train using symmetric ternary neurons
├── DTSQN_test.py          # Test DTSQN model
├── DSQN_train.py          # Train using binary neurons
├── DSQN_test.py           # Test DSQN model
├── pytorch_wrappers.py    # Utility functions and wrappers
└── logs/                  # TensorBoard logs
```
