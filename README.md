[//]: # (Image References)

[image1]: https://user-images.githubusercontent.com/10624937/42135619-d90f2f28-7d12-11e8-8823-82b970a54d7e.gif "Trained Agent"

# Project 1: Navigation

### Introduction

For this project, you will train an agent to navigate (and collect bananas!) in a large, square world.  

![Trained Agent][image1]

A reward of +1 is provided for collecting a yellow banana, and a reward of -1 is provided for collecting a blue banana.  Thus, the goal of your agent is to collect as many yellow bananas as possible while avoiding blue bananas.  

The state space has 37 dimensions and contains the agent's velocity, along with ray-based perception of objects around agent's forward direction.  Given this information, the agent has to learn how to best select actions.  Four discrete actions are available, corresponding to:
- **`0`** - move forward.
- **`1`** - move backward.
- **`2`** - turn left.
- **`3`** - turn right.

The task is episodic, and in order to solve the environment, your agent must get an average score of +13 over 100 consecutive episodes.

### Getting Started
 
You will need to create the proper python virtual environment. The environment specifications can be found in the requirements.txt file in the directory.
Using Anaconda is recommended. To begin, execute the code below from your anaconda command prompt:

$ conda env create -f environment.yaml 

Then navigate to the directory for this project where you downloaded it on your PC and launch jupyter notebook from there.  Proceed to open the Navigation.ipynb file and follow its respective instructions.


### Instructions

The Navigation notebook contains nine sections:

1)	Start the environment
2)	Examine the State and Action Spaces
3)	Take Random Actions in the Environment
4)	Building our NN Model using Pytorch
5)	Building a Replay Buffer for our Agent
6)	Initializing Hyperparameters
7)	Building the Agent
8)	Training the Agent
9)	Watch the Trained Smart Agent

The neural network architecture consists of 2 hidden layers of 64 nodes each and can be seen in section 4.  Experiments involving the addition of additional nodes per layer and the addition of additional layers did not yield improvements in the performance of the agent.
There are two separate replay buffer classes seen in section 5.  The first is a regular (randomly sampled) replay buffer while the second is a prioritized replay buffer.  
There are differing segments of code for learning under the step method in the Agent class seen in section 7.  These segments correspond to using a network architecture of either Deep-Q or Double-Deep-Q and to using a replay buffer in either the randomly-sampled or prioritized scenarios.
The user can select which network and replay buffer are used for training using the appropriate parameters pointed out in section 8.  The user should note that training takes a significant amount of time and may wish to skip to section 9 if additional training isn’t needed.
Finally, the user can watch the successfully trained agent by executing the code seen in section 9.

