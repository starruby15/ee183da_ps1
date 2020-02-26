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

1(c). Function that returns probability: 

### 2.2 Planning Problem 

2(a). State transition function updated for obstacles: 

2(b). Function that returns rewards: 

### 2.3 Policy Iteration 

3(a).  Function that create intial pi: 

3(b).  Function that displays pi: 

3(c).  Function that computes policy evaluation: 

3(d).  Function returns pi under one-step lookahead: 

3(e).  Function that computes policy iteration: 

3(f).  Compute time: 

3(g).  Plot trajectory: 

### 2.4 Value Iteration 

4(a). Value iteration function: 

4(b). Comparing results: 

4(c). Compute time: 

### 2.5 Additional scenarios 

5(a). Exploring values: 





