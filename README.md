# 🌕 Moon Lander AI Agent — Deep Q-Network (DQN)

An AI agent trained using **Deep Reinforcement Learning** to perform autonomous lunar landing in the Gymnasium LunarLander environment. The project uses a **Deep Q-Network (DQN)** to learn optimal actions through repeated interaction with the environment.

**Training Result:** Achieved a reported average reward of **200.10**, meeting the project's configured environment-solving threshold.

## 📌 Project Overview

The objective of this project is to train an intelligent agent that can control a lunar lander and achieve a safe landing. The agent learns through trial and error by interacting with a simulated environment, receiving rewards or penalties, and improving its decision-making policy over time.

This project demonstrates how reinforcement learning can be applied to autonomous control problems without manually defining every action.

## ✨ Key Features

- **Deep Q-Network (DQN):** Uses a neural network to estimate the expected value of available actions.
- **Experience Replay:** Stores past experiences and samples them during training to improve learning stability.
- **Epsilon-Greedy Exploration:** Balances exploration of new actions with exploitation of learned knowledge.
- **Target Network:** Helps stabilize Q-value updates during training.
- **Reward Tracking:** Monitors the agent's learning progress using average episode rewards.
- **Gymnasium Environment:** Trains the agent in the LunarLander simulation.

## ⚙️ How It Works

1. **State Observation:** The agent receives the current state of the lunar lander.
2. **Action Selection:** The agent selects an action using an epsilon-greedy strategy.
3. **Experience Collection:** The state, action, reward, next state, and terminal status are stored in replay memory.
4. **Model Training:** A batch of past experiences is used to update the Q-network.
5. **Target Network Update:** A separate target network helps stabilize the learning process.
6. **Policy Improvement:** The agent repeats this process over multiple episodes to improve its landing performance.

The goal is to maximize cumulative reward while learning effective landing behavior.

## 📊 Training Results

The following average rewards were recorded during training:

| Episode | Average Reward |
|---:|---:|
| 100 | -144.37 |
| 200 | -75.87 |
| 300 | -12.70 |
| 400 | 66.87 |
| 500 | 107.36 |
| 600 | 138.98 |
| 700 | 177.22 |
| 800 | 188.74 |
| 851 | 200.10 |

The training log reports an average reward of **200.10** and indicates that the configured environment-solving threshold was reached. The exact episode count should be interpreted according to the training loop's episode indexing and moving-average calculation.

## 🛠️ Tech Stack

- **Programming Language:** Python
- **Reinforcement Learning Environment:** Gymnasium
- **Numerical Computing:** NumPy
- **Deep Learning Framework:** PyTorch *(confirm against the implementation in this repository)*

## 📁 Project Structure

The exact filenames depend on the files included in the repository.

```text
MOON-LANDER-PROJECT/
├── README.md
├── requirements.txt
├── Training Script / Notebook
└── Model Checkpoint (if saved)
```

Update this structure to match the actual files in the repository.

## 🚀 Installation

### 1. Clone the Repository

```bash
git clone https://github.com/oghacker001/MOON-LANDER-PROJECT.git
cd MOON-LANDER-PROJECT
```

### 2. Create a Virtual Environment

**Linux / macOS**

```bash
python3 -m venv .venv
source .venv/bin/activate
```

**Windows**

```powershell
python -m venv .venv
.venv\Scripts\activate
```

### 3. Install Dependencies

If the repository contains a `requirements.txt` file:

```bash
pip install -r requirements.txt
```

Otherwise, install the packages required by your implementation. A typical Gymnasium DQN setup may use:

```bash
pip install numpy gymnasium torch
```

The LunarLander environment may require additional Box2D dependencies. Refer to the [Gymnasium LunarLander documentation](https://gymnasium.farama.org/environments/box2d/lunar_lander/) if installation fails.

## ▶️ Running the Project

Open and run the training notebook or script included in the repository.

For example, if the actual training script is named `train.py`:

```bash
python train.py
```

Replace `train.py` with the actual filename in your repository.

## 📈 Results and Reproducibility

The reported average reward of **200.10** reflects the available training output. Results may vary across runs depending on random seeds, library versions, and training parameters.

For reproducible experiments, document:

- Learning rate and discount factor
- Replay-buffer capacity and batch size
- Epsilon-greedy exploration schedule
- Target-network update frequency
- Number of training episodes and solving threshold
- Random seed and dependency versions

A reward-versus-episode plot and evaluation over multiple episodes can further demonstrate the agent's performance.

## 🔮 Future Improvements

- Add a separate evaluation script for the trained agent.
- Visualize learning progress with reward curves.
- Evaluate performance across multiple random seeds.
- Save and document the trained model checkpoint.
- Create a short animation of a successful autonomous landing.
- Improve experiment reproducibility through documented configurations.

## 👨‍💻 Author

**Nishant Gupta**

- **GitHub:** [oghacker001](https://github.com/oghacker001)
- **Project Repository:** [MOON-LANDER-PROJECT](https://github.com/oghacker001/MOON-LANDER-PROJECT)

---

*This project explores Deep Reinforcement Learning, value-based learning, and autonomous control in a simulated lunar landing environment.*
