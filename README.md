# RL-Battleship

## Game Rules ##
- Only one player (the RL agent) plays against a programgenerating the battle situation
- All ships take up only a single square
- Ships can touch each other and touch the board border even-tually
- Ships are placed on a 10x10 game board
- Ships take several hits to sink (one take one hit, some take 2,some take 3) 
- The agent wins when all ships are sunk. The goal is to sinkall ships with as few hits as possible

## How to run ##

There are 3 agents were implemented in this project. Go to the main function, specify the number of episodes and choose the agent that you want to run. If you run this notebook on Google Colab and you want to save the figures to your computer, set `download_plots` to `True`.

```python
if __name__ == "__main__":
  number_of_episodes = 3000  # Number of episodes you want to run the agent
  download_plots = False     # "True" if this notebook is running on Google Colab and you want to save the figures to your computer, "False" otherwise
  env = env_generator()

  # Test Q-Learning agent
  env.reset()
  test_Q_Learning(env, number_of_episodes, download_plots)

  # Test SARSA agent
  env.reset()
  test_SARSA(env, number_of_episodes, download_plots)

  # Test DQN agent 
  env.reset()
  dqn = DQN(env)
  dqn.runner(number_of_episodes, download_plots)
```
