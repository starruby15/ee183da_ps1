# Running Code Instructions

The code was developed in Google Collab.  This works by uploading the ipynb file into google drive and using the collab extension to run it.  More here: https://towardsdatascience.com/getting-started-with-google-colab-f2fff97f594c 

Google collab runs python code in code blocks and it does this sequentially.  Meaning the number that appears after hitting the play button indicates the place of that code block in the sequence of runs.  This also means that if a function is run in a code block and the number 5 appears, but there is a previous code block that calls it and the number 3 appears, the previous code block will throw an error because the function was defined/run before it.  All of my code runs in order from top to bottom.  This means if the code is opened in Google Collab on Google Drive, please go down and run the code blocks one by one until hitting the bottom. Otherwise there will be missing functions/variables. 

There is a top module at the very bottom that accepts a probability error and discount: 
top(probability_error, discount)

This will run policy and value iteration and display the initial pi and the final pis found from each iteration. 

# Answers 

### Preliminaries 

0(a). No one 
0(b). Class resources and stackexchange only for python syntax (i.e. classes and np array help) 

### 2.1 MDP System 

1(a). Size of state space Ns = L * H - obstacles = 26

1(b). Size of action space Na = size of {left, right, up, down, none} = 5 

1(c). Function that returns probability: get_probability(s,a,n_s) 
      Note this function has been altered for 2a and is the same now.

### 2.2 Planning Problem 

2(a). State transition function updated for obstacles: get_probability(s,a,n_s) 

2(b). Function that returns rewards: get_reward(s)

### 2.3 Policy Iteration 

3(a).  Function that create intial pi: get_pi_initial()

3(b).  Function that displays policy from pi: display_policy(pi)

3(c).  Function that computes policy evaluation: policy_evaluation(values, pi)
       This function will uses get_value to generate the entries for the value matrix. 
       get_value uses am_i_obstacle(s) to detect if s is an invalid state bc its out of bounds or in an obstacle

3(d).  Function returns pi under one-step lookahead: policy_onestep_lookahead(values,pi)

3(e).  Function that computes policy iteration: policy_iteration() 

3(f).  Compute time: approximately 0.689s 
       This was done by using python timer functions

3(g).  Plot trajectory: shown in 3g.jpg under results folder  

### 2.4 Value Iteration 

4(a). Value iteration function: value_iteration()

4(b). Comparing results: shown in 4b.jg under results folder 

4(c). Compute time: approximately 0.545s
      This was done by using python timer functions

### 2.5 Additional scenarios 

5(a). Exploring values: shown in results folder.

(0.01, 0.9) (original) => robot aims for +10 

(0.01, 0.1) => robot goes for either +1 or +10, but also freezes when there is a high danger zone next to it 

(0.3, 0.1) => robot goes for either +1 or +10, but also freezes when there is a high danger zone next to it. This one is slightly different because the robot has freezes almost everywhere except to +10.

(0.1, 0.3) => robot goes for either +1 or +10, but also freezes when there is a high danger zone next to it. In this one the robot is willing to move down and left for +10 but still freezes 4/6 times. 

(0.4, 0.9) => robot aims for +10, but does freeze when between obstacle and high danger zone 



  

