Assignment 2: 2048
=========

Your task is to implement a game AI for the 2048 game based on simple expectimax search. The game engine is based on the code [here](https://gist.github.com/lewisjdeane/752eeba4635b479f8bb2). 

Due date
-----
Feb-3 11:59pm Pacific Time.

Grading
-----
- Regular Commits (1 points)

You should at least one nontrivial commit by Jan-27 11:50pm. 

- Documentation (1 points)

Comment your code generously. 

- Functionality (10 points)

The player should be modelled as a max player, and the computer modeled as a chance player (picking a random open spot and place a 2-tile). 

Each time, the evaluation function at leaf nodes should be a weighted sum of the following two factors: 

-- The points that can be obtained in at the end of simulation (either the total points or just the additional points from the current position). 
-- The highest tile that can be achived at the end of the simulation. 

You can tune the weights and see if they change the performance. 

In README, write down the statistics of the end score and highest tile for in the following three types of AI (run each 5 times): 

-- Random move. 
-- Computing a depth-1 search tree (i.e., just one max-player move). 
-- Computing a depth-3 search tree (i.e., a max-min-max sequence). 

Note that you can press "u" at the end of a game to undo the last move and see the last configuration. Check more keyboard options by reading the code. 

You should see depth-3 search reaching 512 tiles and a score over 5000 quite often, as shown in the movie file. 

Extra credits (4 points)
------
While depth-3 search gives reasonable performance, it can apparently be improved by searching more depth. As the tree gets bigger, you may need to pay attention to the efficiency of the code -- a naive implementation of depth-5 search may make each decision quite slow. 

You get up to 4 extra points if you can engineer the AI to reach 2048 very often, while each step is reasonably smooth when running on a laptop. 

Note that engineering the evaluation function, for instance by giving some heuristic score for different tile configurations, may help. 

Note
------
- Make sure that you start immediately. You can see that significantly more code is required compared to Assignment 1. 
- At the deadline, Github will automatically save the last commit as your submission. Make sure to commit your full solutions before that. 