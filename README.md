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

## Unit 4: Policy gradient with PyTorch
Q-learning is a value-based method, meaning that the algorithm predicts the value of a given action and the policy just picks the action with the highest predicted value. We can of course also learn the policy directly, the model then gives a probability distribution over the actions. Because of this we don't have to worry about the exploration/exploitation trade-off. An additional benefit is the ability to deal with high dimensional and even continuous action spaces. So in this unit we developed the Monte Carlo Reinforce algorithm from scratch and trained it on some basic environments.

https://user-images.githubusercontent.com/26146888/222951342-3c6d35e5-5b90-4489-bbc8-739af145fdd0.mp4

## Unit 5: Unity ML-agents
Games like we worked in before can only get complex to a certain point, to go further you need a game-engine (if you don't want to spend a long time developing an environment). In this chapter we therefore looked at how we can train RL agents in the Unity game engine.

![snowballs](https://user-images.githubusercontent.com/26146888/222951496-d2c59893-2125-4191-a855-b85cd97c7849.gif)
![pyramids](https://user-images.githubusercontent.com/26146888/222951506-97a41dee-880c-41c4-94e3-01da588c0b9c.gif)

## Unit 6: Actor Critic methods in robotics environments
An issue with Monte Carlo Reinforce and similar algorithms is that there is a lot of variance when computing the gradients, meaning that the training is a lot slower. Actor-Critic methods are hybrids combining an Actor which determines the policy (policy-based method) with a critic that determines how good an action was (value-based method). Through this solution the variance is reduced and the algorithm can therefore move more quickly towards the optimum. We applied the Advantage Actor Critic (A2C) method on some robotics environments in this unit.

https://user-images.githubusercontent.com/26146888/222951762-2daaa039-e4c8-454b-97c1-408c0955ce1d.mp4

## Unit 7: Multi-agent and AI-vs-AI
In this unit we learned about different methodologies to train multi-agent systems, both cooperative and competitive. The main challenge in this unit was to train a football team of two players that would go up against teams trained by others following this course. At the time of writing this my best team has moved up from place 176 to place 40 on the leaderboard, hopefully we can climb a bit further :raised_hands: Below you can see two of my teams playing against each other.

![soccer](https://user-images.githubusercontent.com/26146888/222952066-6eab44c1-12ae-4800-89c1-5b9671db5bc9.gif)

## Unit 8: Proximal Policy Optimization
This unit exists of two parts, where we dove into the PPO algorithm. One of the core ideas behind PPO is that it is better to be conservative in the policy updates. Smaller policy updates have a larger chance of leading to an optimal policy, while larger updates could fall from a cliff which is hard or impossible to recover from. However, the steps shouldn't be too small either as the training process becomes very slow. PPO therefore uses a Clipped Surrogate Objective function, which clips the updates to the policy. PPO also incorporates the actor-critic approach. We applied PPO to multiple environments, including VizDoom.

https://user-images.githubusercontent.com/26146888/225720676-e8423309-772a-46cd-9eb9-0459ed95df5b.mp4

After unit 8 there was some more bonus content with some theory on advanced topics and pathwas to dive into those. With that, I've come to the end of the course achieving the certificate of excellence for completing every challenge. It's a really interesting and fun course that I can certainly recommend!

