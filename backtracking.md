# Recursive Backtracking
Written for CS 106B, Spring 2019 taught by Julie Zelenski and Marty Stepp

## Why use backtracking?

The word 'backtracking' refers to a specific class of recursive problem-solving, where our recursive subproblems have a special relationship. In particular, our sub-problems are related by the different *decisions* that we can make from some *state*.

The *state* is the collection of decisions that have been previously made, the partial solution we've built up, and any other information our recursive function needs to make decisions. The state is defined by the parameters we pass into our function.

What a *decision* looks like can vary based on the type of problem. Some common examples are: `TODO`

The execution of our recursive function can be drawn as a *decision tree*, where each node is function call (with a given state from its parameters) and each branch is a decision by that function.

### Types of Backtracking Problems
*Note: these names/groups may change quarter by quarter, but they have similar structure*
- Backtracking (finding any solutuion)
- Optimization (finding the **best** solution)
- Combinations (order doesn't matter)
- Permutations (order **does** matter)

## Outline For Implementation

Writing a backtracking function can often be described by three steps: choose, explore, and unchoose. We will also talk about how to write good recursive base cases.

### Choose

1. Recursion involves iterating. What are you iterating over?
2. Does the order you iterate matter?
  - E.g. are you iterating over a subset or a list?
3. What are the choices you have for each item?

### Explore
4. How can I represent my choice?
- Change the state by modifying your parameters!

5. What do I do with the return value from a recursive function?
- How does the answer to the smaller problem influence your larger problem?
- Each smaller problem represents a decision made. Is your goal to see if that decision was successful? Do you make every decision regardless of the return value?

5a. Am I using arms-length recursion? 
- Are my choices at this levvel, or am I "reaching into" the next recursive call?

### Unchoose
6. Need to undo the choices from Step 4. This must happen before the next choice at this level is made, so our function should look like a miror image around the recursive call.

### Base Cases:
7. Do I have a base case for when I'm out of things to iterate over? (See 1.)
8. Do I have a base case for when I'm out of valid choices/a bad state is reached?
- Does my function need to return different things (e.g. `true` and `false`) depending on whether the call was successful?

Often times, backtracking questions will present you with two data structures. One data structure can be used to make decisions, while the other contains objects that will interact with the decisions being made. Sometimes, if we have few decisions (e.g. a problem with two known options) we don't have an explicit data structure, but it is important to think about waht decisions are available for each state!

When drawing a decision tree for a given problem, remember that traversing horizontally across the three goes through the decisions that can be made at each node, while traversing down the tree represents repeated recusrive calls. `TODO`

Let's look at more examples. `TODO`

## Beware the Curse of "Arms-Length Recursion"

The difference between "correctness" and "validity" for a state.

`Made with <3 by Peter Maldondao, with inspiration from Ashley Taylor`
