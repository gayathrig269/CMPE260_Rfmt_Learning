# CMPE260_Rfmt_Learning
To train or teach a computer on how to play the game of Tic-Tac-Toe using different Reinforcement Learning concepts like Min Max algorithm to Neural Networks. 

Agent – Player of the game, either Min-Max agent, Tabular Q agent, or Neural Network agent. 
State – State of the game when a player makes move.
Action – Marking a Cross or a Naught on the game board.
Environment – The space where agent moves, it will be a 3X3 Tic-Tac-Toe board.
Policy – The algorithm used, either Tabular Q Learning or Min-Max in deterministic fashion.
Reward/Punishment – A player wins or loses the game.


# Part 0:
Setting up a 3X3 Tic-Tac-Toe board.

# Part 1: Min-MAx 
Using Minimum-Maximum algorithm, train the agent to play against Random Player and itself. 

Min-Max Strategy:
1. Assumptions
   Make the best move (max. game value for us)
   Opp. will also make the best move.(min. the game value for us)
2. Internal cache storage – game board position. Compute all possible continuations from a given position only once. 
Results are plotted and statistics is taken for conclusion.


# Part 2: Tabular QLearning
Using Tabular Q Learning policy, training the agent to perform better than Min-Max agents and Random player.Results are plotted and statistics is taken for conclusion.

Tabular Q Function : 
By looking up the Q values for all possible moves in the current situation and chose the one with the highest value. 
Rewards
Best move -1
Loss - 0
Draw – 0.5
Learning rate(alpha) – 0.9 and (Discount factor)gamma – 0.95


# Part 3: Neural Network Q Learning 
QLearning strategy used, a # Neural Network is built to play against other agents.  

We implement the Neural Network Q Learning player in the following way:

  1. An input layer which takes a game state, i.e., the current board, as input.
  2. One or more hidden layer.
  3. An output layer which will output the Q value for all possible moves in that game state.
  4. We use Mean Squared Error as our loss function, which is a generic and popular loss function for regression, i.e., learning to mimic another function.
  5. The input for the loss function will be the output of the Neural Network and our updated estimate of the Q function by applying the discounted rewards and maximum Q     values of the next states. i.e., the loss will be the difference between the output of the Neural Network and our updated estimate of the Q function.
  6. We use the Gradient Descent Optimizer for training — i.e., to adjust the weights in the Neural Network. 
  7. We use ReLu activation function.

Used other activation functions like tanh,sigmoid,leaky reLU and other optimzer- Adam. Experimented with Epsilon parameter to use less greedy approach. Plots against every RL agent is analysed for every battle. 
