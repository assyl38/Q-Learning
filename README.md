# Q-Learning
## Important terms

| Term | Description |
| --- | --- |
| `State` |  The current position/condition retrned by the model. |
| `Action` |  All the possible steps that can be taken by the model and it picks one action. |
| `Rewards` |  To help the model move in the right direction, it is rewarded / points are given to appraise some action. |
| `Episodes` | When an agent ends up in a terminating state and can’t take a new action. |
| `Q-Values` | Used to determine how good an Action, A, taken at a particular state, S, is. Q (A, S). |
| `Temporal Difference` | A formula used to find the Q-Value by using the value of current state and action and previous state and action. |

## Bellman Equation

The Bellman Equation is used to determine the value of a particular state and deduce how good it is to be in/take that state. The optimal state will give us the highest optimal value. 

The equation is given below. It uses the current state, and the reward associated with that state, along with the maximum expected reward and a discount rate, which determines its importance to the current state, to find the next state of our agent. The learning rate determines how fast or slow, the model will be learning.


<p align='center'>
<img width="600" height="200" src="https://www.simplilearn.com/ice9/free_resources_article_thumb/6-bellman.JPG"> </br>
<em>Figure 1: Bellman Equation   </em>
</p>

## How to make a Q-Table?
While running our algorithm, we will come across various solutions and the agent will take multiple paths. How do we find out the best among them? This is done by tabulating our findings in a table called a Q-Table. </br>

A Q-Table helps us to find the best action for each state in the environment. We use the Bellman Equation at each state to get the expected future state and reward and save it in a table to compare with other states. </br>

Lets us create a Q-table for an agent that has to learn to run, fetch and sit on command. The steps taken to construct a q-table are :</br>

Step 1: Create an initial Q-Table with all values initialized to 0 </br>

When we initially start, the values of all states and rewards will be 0. Consider the Q-Table shown below which shows a dog simulator learning to perform actions : </br>

<p align='center'>
<img width="421" height="203" src="https://www.simplilearn.com/ice9/free_resources_article_thumb/7-initial.JPG"> </br>
<em>Figure 2: Initial Q-Table    </em>
</p>

Step 2: Choose an action and perform it. Update values in the table </br>

This is the starting point. We have performed no other action as of yet. Let us say that we want the agent to sit initially, which it does. The table will change to: </br>

<p align='center'>
<img width="421" height="203" src="https://www.simplilearn.com/ice9/free_resources_article_thumb/8-qtable.JPG"> </br>
<em>Figure 3: Q-Table after performing an action    </em>
</p>

Step 3: Get the value of the reward and calculate the value Q-Value using Bellman Equation </br>

For the action performed, we need to calculate the value of the actual reward and the Q( S, A ) value </br>

<p align='center'>
<img width="421" height="203" src="https://www.simplilearn.com/ice9/free_resources_article_thumb/9-updatingq.JPG"> </br>
<em>Figure 4: Updating Q-Table with Bellman Equation  </em>
</p>

Step 4: Continue the same until the table is filled or an episode ends </br>

The agent continues taking actions and for each action, the reward and Q-value are calculated and it updates the table. 

<p align='center'>
<img width="421" height="203" src="https://www.simplilearn.com/ice9/free_resources_article_thumb/10-finalq.JPG"> </br>
<em>Figure 5:  Final Q-Table at end of an episode </em>
</p>



## Credits
* [What Is Q-Learning: The Best Guide To Understand Q-Learning](https://www.simplilearn.com/tutorials/machine-learning-tutorial/what-is-q-learning?utm_campaign=WhatisQLearning&utm_medium=Description&utm_source=youtube) 
