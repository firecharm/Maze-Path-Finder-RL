# MMAI 894 RL Project:
Maze-path-finder

## Getting Started
These instructions will get you started on playing around with the environment and config the algorithm

### Environment:
from MazeEnv import MazeGen maze = MazeGen(num_x, num_y) maze.render()

random_start not in place yet.

Available functions are maze.reset(), maze.set_grid(), maze.set_reward(), and maze.render(). Use maze.set_reward() to change reward of Star (default 10), Trap (default -10), and Step (default -1). The default reward for Terminal is 100.

Use maze.set_grid() to add Star, Trap, or reset Player, and Terminal. Default num of Player and Terminal are one. !! Adding Stars will significantly increase the complexity of this problem. As adding stars will significantly increase dimensions of states. Adding traps will not cause this issue.

Use maze.render() to plot.

### Algorithm
MultiArmBandit : alg = MultiArmBandit(maze) alg.render() alg.run_algorithm()

MarteCarlo: alg = MonteCarlo(maze, discount = 0.9, epsilon=0.2) # epsilon controls the scale of exploration, discount controls how much return cares for future actions alg.render() alg.run_algorithm(10000)

alg.plot_last_episode() # use this to plot the last episode, not necessarily the best. Codes need modification to record all results.

SARSA: alg = SARSA(maze, discount = 0.9, epsilon=0.1, alpha = 0.9) # epsilon controls the scale of exploration, discount controls how much return cares for future actions, alpha controls the step size alg.render() alg.run_algorithm(10000)

alg.plot_last_episode() # use this to plot the last episode, not necessarily the best. Codes need modification to record all results.