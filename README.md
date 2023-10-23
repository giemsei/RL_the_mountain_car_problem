# RL_the_mountain_car_problem

## MCE:
LANDSCAPE: `np.sin(3 * xs) * 0.45 + 0.55`

Transition dynamics: `velocity += (action - 1) * self.force + math.cos(3 * position) * (-self.gravity)`

## MCE2:
LANDSCAPE: `0.3*np.sin(4*xs+np.sqrt(np.sin(10*xs)+2))+0.5`

Transition dynamics: `velocity += (action - 1) * self.force + (0.3 * np.cos(4*position + np.sqrt(np.sin(10*position) + 2)) * (4 + (5 * np.cos(10*position)) / (2 * np.sqrt(np.sin(10*position) + 2)))) * (-self.gravity)`

> So the slides presentation of the models are going to be avaible on lastminuteanalysis.com after the exam

## Index

In order to solve the mountain car problem we are going to use 
- the Q-learning algorithm
- Sarsa Algorithm
- Expected Sarsa Algorithm

To obtain clearer insights from the data, we averaged the reward results over buckets of 500 episodes, utilizing the `SHOW_EVERY = 500 parameter`. This approach helps in reducing noise in our outcomes, allowing us to discern patterns more effectively. However, it might be insightful to also examine data in smaller episode buckets for a finer-grained analysis.

For the second file (in the file MCA - Mountain Car Agent):
To evaluate the efficacy of the algorithms, we focused on the graphs representing the `max-rewards` from the last `100 buckets`. This decision was based on previous analyses which suggested that this metric displayed the least noise. In distinguishing the performance differences among the algorithms, we pinpointed the one that consistently delivered superior results.

