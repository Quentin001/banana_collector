### Purpose

In this project a Deep Q-Network Agent is trained to collect yellow bananas and avoid blue bananas.

### Description

The environment is a three dimensional continuous square world running in Unity, containing yellow and blue bananas.

In this environment, an agent is trained with a Deep Q-Network algorithm to collect the yellow bananas and avoid the blue bananas.
The action space contains 4 actions: 

* 0: walk forward
* 1: walk backward
* 2: turn to the left
* 3: turn to the right

and the state space is a continuous space of dimension 37 representing the velocity of the agent and the ray-based perception of objects around the forward direction of the agent.

The reward function simply returns +1 for collecting a yellow banana and -1 for collecting a blue banana.

### Installation
The instructions below are tested under Ubuntu 18.04. They are from https://github.com/udacity/deep-reinforcement-learning/tree/master/p1_navigation where you will find instructions for Windows and MAC too.

#### Clone the following project from github
´´´git clone https://github.com/udacity/deep-reinforcement-learning.git´´´
´´´cd deep-reinforcement-learning/python´´´
'''
#### Create a virtual environment for the project dependencies
python -m virt_env ./virt_env

#### Activate the virtual environment
source virt_env/bin/activate

# Install dependencies
pip install .

#### Download the Unity environment
Click the link corresponding to your operation system at https://github.com/udacity/deep-reinforcement-learning/tree/master/p1_navigation
under "Getting started", and download the file in the p1_navigation/ folder in the GitHub repository, and decompress it.

#### Run the Jupyther notebook 
Copy the file proj_1.ipynb from my github repository in your p1_navigation/ folder and from that folder run the following command:
jupyter notebook proj_1.ipynb

### Architecture
The agent brain is a Deep Q-Network with three layers (class QNetwork), that learns to output optimal actions in a Deep Q-Network algorithm (function dqn).

### Results
The learning requires less than 500 episodes (after around 500 episodes of 1000 actions, the agent usually gets an average score, computed over the last 100 consecutive scores,
that is superior to 13).

After the learning phase, the trained agent is tested at the end of the notebook. The agent shows clearly its ability to collect yellow bananas and avoid blue bananas.


