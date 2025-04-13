# 🧠 Deep Reinforcement Learning for Portfolio Optimization using PPO

This project demonstrates how to apply Deep Reinforcement Learning (DRL) using Proximal Policy Optimization (PPO) to optimize a portfolio consisting of multiple stocks. It draws inspiration from the article [Deep Reinforcement Learning for Portfolio Optimization](https://thepythonlab.medium.com/deep-reinforcement-learning-for-portfolio-optimization-unleashing-the-power-of-proximal-policy-ffaed37cbcd4) by The Python Lab.

## 📈 Project Summary

The core objective is to maximize returns by training a reinforcement learning agent to make intelligent trading decisions—buy, sell, or hold—based on historical stock data.

### Key Features
- ✅ Proximal Policy Optimization (PPO) algorithm
- ✅ Custom environment modeled for trading with multiple assets
- ✅ Portfolio state representation (stock prices, cash balance, etc.)
- ✅ Reward shaping based on portfolio growth
- ✅ Evaluation of the agent post-training

---

## 📂 Project Structure

portfolio-optimization-ppo/ ├── data_fetching.ipynb # Downloading stock data using yFinance ├── environment.py # Custom trading environment ├── agent.py # PPO model and policy network ├── training_loop.ipynb # Full training script ├── evaluation.ipynb # Post-training evaluation loop ├── requirements.txt # Python dependencies └── README.md # Project documentation


---

## ⚙️ How It Works

### 1. **Environment Setup**

The environment takes in historical stock prices (AAPL, GOOGL, WMT, TSLA), simulates trading episodes, and provides the agent with:
- Portfolio state: stock prices + cash balance
- Reward: profit or loss after each action
- Action space: Buy, Sell, or Hold for each stock

### 2. **The Agent (PPO)**

We use a neural network to model:
- **Actor**: Outputs probabilities of taking each action
- **Critic**: Estimates the value function for better policy updates

### 3. **Training Loop**

The agent:
- Observes state
- Chooses an action based on PPO policy
- Receives a reward and new state
- Optimizes the model using the clipped surrogate objective from PPO

### 4. **Evaluation**

After training, the agent is evaluated on unseen data to assess portfolio performance over multiple episodes.

---

## 🚀 Getting Started

### Prerequisites

```bash
pip install -r requirements.txt



Run the Notebooks
Download Data:
Run data_fetching.ipynb to collect historical data using yFinance.

Train the Model:
Run training_loop.ipynb to train the PPO agent.

Evaluate:
Run evaluation.ipynb to test the trained model.

📊 Results
The trained agent learns to allocate resources efficiently across multiple stocks, balancing risk and return using historical trends.

Performance is measured by the total reward and portfolio value across evaluation episodes.

📚 References
The Python Lab Article

OpenAI PPO Paper

TensorFlow

yFinance

🧠 Author
Harsh Panday
If you found this project useful, give it a ⭐ and feel free to connect!

📜 License
This project is licensed under the MIT License - see the LICENSE file for details.

yaml
Copy
Edit

---

Let me know if you'd like a `requirements.txt` file generated or help creating the GitHub repo structure.
