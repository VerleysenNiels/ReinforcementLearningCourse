# Reinforcement Learning Course
Following along the course on Deep Reinforcement Learning by Huggingface (hosted [here](https://huggingface.co/deep-rl-course/unit0/introduction?fw=pt))

## Unit 1: Intro to RL
Using proximal policy optimization (PPO) to solve the lunar lander gym environment. PPO is a policy gradient method published [by OpenAI in 2017](https://openai.com/blog/openai-baselines-ppo/) with the aim to balance implementation difficulty, efficient sampling and ease of tuning. The method is very easy to use through the stable baselines library. I ended up with a trained agent achieving a score of 267.75 (placing 178th out of 1591 entries at the time of writing).

https://user-images.githubusercontent.com/26146888/208782819-7dd15e2e-41c7-4e3c-86b9-8dcad1b0bb90.mp4

## Unit 2: Q-learning
The second unit took a deeper dived into value-based methods, with a focus on Q-learning. Value-based methods estimate the value of a state (V) or the value of an action in a state (Q). The Q stands for quality. The very basic Q-learning method uses a table where we keep track of the value of each action in each state. These values are updated via the Bellman equation when exploring the environment. We applied this on some standard examples.

https://user-images.githubusercontent.com/26146888/209931837-36e02d45-56fc-4364-b067-8c4c85bf8d09.mp4

## Unit 3: Deep Q-Learning
Of course Q-tables don't scale very well when the environment starts to become more complex. The solution is to use a Q-value estimator, for instance a neural network. After the theory we applied this technique through a library. Sadly enough we did not get to implement our own DQN. Luckily I already [did this a couple of years ago](https://github.com/VerleysenNiels/Q-Learning). I was still learning how to develop neural networks then, but I gained a lot of insights by implementing different DQN papers. On the leaderboards I ended up 190th and 11th (out of ~400 and 17 respectively), the difference between the leaders and the others came down to compute power. As reinforcement learning keeps improving by interacting with the environment, the longer you train the model the better it can become.

https://user-images.githubusercontent.com/26146888/209936560-ac194564-0868-4c57-8730-216e42714f90.mp4

