![1_VMx4SIPmc05UVreQP8N9Sw](https://user-images.githubusercontent.com/78098329/182009675-7a7c967e-8a48-4977-ab5e-2735c430cac8.png)

Introduction:
Have you ever wondered what a Moore Machine is and how it works? If not, don’t worry you are at the right place. Here in this blog, we are going to study how a Moore machine can be implemented by OOP.

A Moore machine is a Finite State Machine(FSM) where output depends on the current state.

Moore Machine is a Finite Automata with output.

Moore Machine output is synchronous

It’s a machine where the next state is decided by the current input state and input symbol.

The Moore Machine is denoted by 6 tuples.

Description of the Moore Machine is (Q, q0, ∑, O, δ, λ’) where

Q: Finite set of States

q0: Initial State

∑: Finite set of Symbols

δ: Transition Function, it is also defined as Q × ∑ → Q

O: Output alphabet

λ’: Output function where Q → O

Here, we have developed a Moore machine in C++ to give the remainder obtained by dividing a number by 3.

## Transition Table for the Moore Machine
![image](https://user-images.githubusercontent.com/78098329/182009749-4276c187-c3e1-4d06-ab73-eecf5530bfae.png)

## Transition State Diagram for the Moore Machine
![image](https://user-images.githubusercontent.com/78098329/182009759-95fbdaeb-eb64-4e11-b755-73d3a4854bdc.png)

Following is the code for constructing a Moore Machine in C++ using Linked List:

# class.cpp


This file consists of the creation of a class “Node” which is going to represent a state in the Moore Machine.

transition0: represents the transition from a given state when the input character is 0, it is in the form of the pointer from the given node.

transition1: represents the transition from a given state when the input character is 1, it is in the form of the pointer from the given node.

value: consists of output value for each and every state as per the definition of the Moore Machine

finalState: a global variable that will be having the final output state of the Moore Machine

![carbon (4)](https://user-images.githubusercontent.com/78098329/182009593-cdc5cebe-a703-49f6-ac37-740106009f1e.png)


# makeTransition.cpp

It is a recursive function that is called until we reach the end of the string, where input parameters are the current state of the machine denoted as temp, the current index of the string, and the string itself.

This function is created in such a way that when we reach the end of the string we terminate the function after assigning the finalState to the last state of the machine so that we can get the desired output.

If the string is not yet terminated we will make the ‘0’ and ‘1’ transition respectively as per the current character of the string.

At the end of the function, we have to make the next transition by incrementing the index and passing the next state as shown in the code.

![carbon (5)](https://user-images.githubusercontent.com/78098329/182009617-71ffa209-ce8c-4472-a0a7-acc5d515e6ca.png)


# initializeMooreMachine.cpp

This function initializes the transitions for each and every state based on the transition table in Fig 1.1 and transition diagram in Fig 1.2

Here the states are passed using double pointers which means the reference to the pointers to ensure proper changes are made in the memory of each state.

![carbon (6)](https://user-images.githubusercontent.com/78098329/182009662-0bc44b90-b4da-4517-9467-588d67557dcc.png)


# main.cpp

This is the main file where we initialize the three states as per Fig 1.2 with desired outputs for every state.

Later we call the initializeMooreMachine function, after that, we take the binary string from the user to pass it through the Moore machine.

After taking input the string is passed through the Machine using the makeTransition function.

After reaching the final character of the string we get the finalState, so we can simply print the value of that state which is the desired output of our machine.

![carbon](https://user-images.githubusercontent.com/78098329/182009477-fbbaa174-43ac-492f-a500-05950f696e7a.png)


![image](https://user-images.githubusercontent.com/78098329/182009792-32d9c2b0-60e1-45b1-b6e1-e34e58347618.png)



# Conclusion
From this, we can conclude that finite automata could be implemented by using various programming languages. By implementing it through programming Language we are able to figure out how internally our computers work. In our previous blog, we studied the Theory of Computation principles and we learned about Finite automata and its type and Regular and Non-Regular expressions. In this blog, we have implemented finite automata through OOP using C++. Our computers are nothing but this combinational and sequential circuit that has been implemented by the principle of finite automata.

