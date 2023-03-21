# Policy-Gradient-in-Mujoco
## Intorduction
The repo is the assignment 3 of cs234 winter 2023 from Stanford University.
The project works on establishing a policy network to train the simulation environment, cartpole, pendulum, and cheetah. The network aims to maximize the reward collected from each environment. 
## Methods
The policy networks use categorical and gaussian policy based on the environment action space. And the policy gradients include training without baseline network, training with baseline network, and proximal polixy opimization with baseline network. 
## Results
All the logs and plots are placed in result folder. All methods reach an average reward of 200 on Cartpole, 1000 on Pendulum, and 200 on Cheetah at some point. Some interesting takeaways, adding baseline term will make the training more robust, since in theory, the advantage term will not always be positive, thus resulting in reducing the high variance in the gradient. In addition, ppo training is the most consistent methods among the three methods. The training is able to find the best point for the improvement in the bounded region (old policy network) for the smoother and faster convergence.