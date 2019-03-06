Language:
Python 2

IDE I used: 
Jupyter (Python)

OS I used: Mac OS

How to run code:
Make sure you have python 2.7 installed:
Python 2.7 :: Anaconda custom (x86_64)
iPython 6.1.0
Homebrew and pip
Anaconda - jupyter
	- code is saved as ipynb file Anaconda Notebook

Necessary Libraries (can also be installed with conda):
Numpy  - pip install numpy
Pandas  -  pip install pandas
Seaborn  - pip install seaborn
Matplotlib  - brew install pkg-config, 
    - pip install matplotlib
Scikit-learn - pip install -U scikit-learn
SciPy - pip install scipy
pymdptoolbox - pip install pymdptoolbox

# Markov Decision Processes
This will showcase two MDP problems modeling a gridworld and a modified 'yahtzee' inspired dice game.

## Gridworld
In this MDP I try to model a more simple and traditional path finding problem with a slight twist
on movement. I define a 5 by 5 grid world with cells that have positive and negative reward for
landing on them. An agent is placed at the bottom of the board and has to make its way up
toward the reward square. Its movement is limited to one unit to the left, right, and up. If the
agent tries to move off the board, it is bounced back to its current position. The alteration I made
to the movement is the slight possibility of overshooting. With probability p, the agent will move
1 space but with probability 1-p, it will overshoot and travel 2 spaces in the chosen direction
(unless it would be placed outside the board). The board is shown below.

## Yahtzee Simplified Die Game
This Markov Decision Process is inspired by the game Yahtzee in which a player has 3 tries
to roll dice in order to score points depending on what the final outcome is. In my version, the
player first rolls two dice, one blue and one red. The player then has two more opportunities to
either reroll the blue die, the red die, both die, or neither. After the 3 tries have been used, the
player is awarded points depending on the values on the dice. If the dice match, the player is
awarded 10 points, otherwise, the player is awarded points equal to the value on the blue die
minus the value on the red die.
Generate a MDP example based on a modified yahtzee inspired die game.
    This function is used to generate a transition probability
    (``A`` × ``S`` × ``S``) array ``P`` and a reward (``S`` × ``A``) matrix
    ``R`` that model the following problem. 
    The game is managed by two dice numbered {1-6} with each turn consisting of 
    four actions:
    - Re-roll blue die {action 0}
    - Re-roll red die  {action 1}
    - Re-roll both     {action 2}
    - Re-roll None     {action 3}
    
    An action is decided with the objective to maximize the final score 
    at the final state when the number of turns are over.
    
    Let {0, 1 . . . ``S``-1 } be the states of each turn and the resulting dice rolls.
    
    
    The transition matrix ``P`` of the problem can then be defined as follows:


