# Markov Decision Processes
This will showcase two MDP problems modeling a gridworld and a modified 'yahtzee' inspired dice game

## Yahtzee Simplified Die Game
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
