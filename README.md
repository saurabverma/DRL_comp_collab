# DRLND Competetion and Collaboration Project

NOTE: Readers are requested to please excuse the `90`MB of the `Report` file, which takes about `30`s to load. The big size of the file is because I was trying to examine the state values by printing directly (Section 7), meanwhile I realized the agent just started learning very well so I didn't stop the learning. Hence, the state values printed out takes a lot of file size.

To examine the results in a faster manner, reader may refer to `output.log`, `output.pdf` or `rewards.png` files.

## Project Description

### Environment

In this environment, two agents control rackets to bounce a ball over a net.
If an agent hits the ball over the net, it receives a reward of +0.1.
If an agent lets a ball hit the ground or hits the ball out of bounds, it receives a reward of -0.01.
The goal of each agent is to keep the ball in play.

### State

The observation space consists of 8 variables corresponding to the position and velocity of the ball and racket.
Each agent receives its own, local observation.

### Action

Two continuous actions are available, corresponding to movement toward (or away from) the net, and jumping.

### Aim

The task is episodic, and in order to solve the environment, your agents must get an average score of +0.5 (over 100 consecutive episodes, after taking the maximum over both agents). Specifically,

- After each episode, we add up the rewards that each agent received (without discounting), to get a score for each agent. This yields 2 (potentially different) scores. We then take the maximum of these 2 scores.
- This yields a single score for each episode.

The environment is considered solved, when the average (over 100 episodes) of those scores is at least +0.5.

## Setup

1. Unzip the required environment for your machine (in this project folder):
    - Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Linux.zip)
    - Linux (headless): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Linux_NoVis.zip)
    - Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis.app.zip)
    - Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Windows_x86.zip)
    - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Windows_x86_64.zip)
2. Setup virtual environment (inside this project folder)
```
$ virtualenv ENV
$ . ENV/bin/activate
```
3. Install dependencies:
```
$ pip3 install --user jupyter numpy mlagents matplotlib torch
```
4. Run Jupyter Notebook
```
$ jupyter notebook
```
A web-browser with all the required files should open up automatically now.

## Usage

Open `Report.ipynb` notebook in the web-browser (using jupyter notebook) and run
the commands as described in the file.

For training the model, mark the flag `train_flag=True`.
Once proceeding with the code in the notebook file, this setting with train the
model designed and store the weights as `checkpoint.pth`.

For simply testing the performance of the trained model, simply set
`train_flag=False`.
This setting will assume that `checkpoint.pth` is present and test the
respective model's performance, when code in the notebook file is run.

## References

- [1] https://github.com/udacity/deep-reinforcement-learning
- [2] https://github.com/saurabverma/DRL_cont_ctrl