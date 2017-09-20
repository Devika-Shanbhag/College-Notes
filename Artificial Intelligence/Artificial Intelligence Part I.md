# Artificial Intelligence Part I
## Intelligent Agents
### What is an agent?
* An **agent** is an entity that
	* **perceives** its enviroment through sensors (e.g. eyes, ears, cameras, sensors)
  	* **acts** on its environment through effectors (e.g. hands, legs, motors)
* A **rational agent** is one which does the right thing.
  	* **Rational action:** action that is expected to maximize its performance measure, given the evidence provided by the percept sequence and whatever built-in knowledge the agent has.
  	* **Rationality** depends on:
    	* Performance measure that defines the criterion of success
    	* Actions that the agent can perform
    	* Percept
    	* Environment (States)
* An **autonomous agent** does not rely entirely on built-in knowledge about the environment. It adapts to the environment through experience i.e. *learning*.
* An **agent program** is a function that implements the agent mapping from the percepts to actions.

### Types of Agents
#### Simple Reflex Agent
1. Find the rule whose condition matches the **current** situation (as defined by the percept).
2. Perform the action associated with that rule.
3. Very limited intelligence.
4. Suitable when environment == **Fully Observable**.

#### Reflex Agents with States (Model-Based)
1. Find the rule whose condition matches the current situation (as defined by the percept and the current state).
2. Perform the action associated with that rule.
4. Can work on **Partially Observable** environment.

**Note:** The *state* is a description of the current world environment. It contains all the necessary information to predict the effects of an action and to determine if the state is a goal state.

#### Goal-Based Agents
1. Find the action that will get me closer to the goal state from my current state.
2. Perform that action.

**Note:** A *goal* can be specific (explicit destination), abstract (speed, safety) or numerous.

#### Utility-Based Agents
* There may be many action sequences that can achieve the same goal.
* Which action sequence should the agent take?
 	* The one with the maximum utility i.e. lowest cost.
* Maps a *state* onto a real number which describes the associated degree of happiness.

### Types of Enviroment

* **Accessible (vs Inaccessible):**
* **Deterministic (vs Non-Deterministic / Stochastic):** 
* **Discrete (vs Continuous):**
* **Episodic (vs Sequential):**
* **Observable (vs Partially-Observable):**
* **Single agent (vs Multiple agents):**
* **Static (vs Dynamic):**

## Problem Formulation
### Problem-Solving Agent
* Rational Goal-Based Agent
 	* Performance measure is defined in terms of satisfying goals.
#### Steps
1.	**Goal Formulation**
	- Define and organise objectives (goal states)
2.	**Problem Formulation**
	- Define what states and actions (transitions) to consider.
3.	**Search for a Solution**
	- Find a sequence of actions that lead to a goal state.
	- No Knowledge → Random Search
	- Knowledge → Directed Search
4.	**Execution**
	- Actually carry out the recommended actions.
	
### Types of Problems
1. **Single-State Problem**
	- accessible world state (sensory information is available)
	- known outcome of action (deterministic)
2. **Multiple-State Problem**
	- inaccessible world state (with limited sensory information) i.e. agent only knows which set of states it is in
	- known outcome of action (deterministic)
3. **Contingency Problem**
	- limited or no sensory information (inaccessible)
	- limited agent knowledge, action result is not predictable
	- effect of action depends on what is found to be true through perception/monitoring (non-deterministic)
	- problem solving requires sensing during the execution phase
4. **Exploration Problem**
	- no information is known about the world state or outcome of action
	- experimentation is often needed
		- hypotheses as actions, search in the real world
		- *learning* builds the agent's knowledge of states and actions progressively
