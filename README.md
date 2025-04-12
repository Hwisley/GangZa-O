# GangZa-O (오강자)

<p align="center"><img src="https://user-images.githubusercontent.com/80737049/172663329-43d0c6cc-a16e-4bc7-97f7-bbddd02d7e96.jpg"/>
<br> - GangZa-O (AI, 1 months old) -
                    </p>

GangZa-O was developed during an AI Bootcamp in 2022, where I led a team of five members in implementing reinforcement learning solutions. 

The project name "GangZa-O" reflects two meanings: the agent's name "GangZa O" and the Korean phrase meaning "five strong individuals."

### Technical Stack
- **Programming Languages & Frameworks**: Python, PyTorch
- **Machine Learning**: Deep Q-Network (DQN), Reinforcement Learning
- **Data Processing & Visualization**: Pandas, Matplotlib
- **Cloud Infrastructure**: Google Cloud Platform (GCP)

### Project Results:

<table align='center'>  
<tr>
<td>
<div>
<img src="https://user-images.githubusercontent.com/80737049/172748092-652ca0d2-08d8-4f29-8d82-175e31bff183.gif" width="85%" height="85%">

</div>
</td>
<td>
<div>
<img src="https://user-images.githubusercontent.com/80737049/172748583-9d3c7daf-6acf-4954-8c76-f6e4b77d8493.gif" width="90%" height="90%">

</div>
</td>
</tr>
<tr>
<td>
<div>
Early-stage GangZa demonstrating unintended behavior by actively avoiding items. 😇😇😇😇😇
</div>
</td>
<td>
<div>
Advanced GangZa showcasing optimal item collection behavior after successful training. 🧡
</div>
</td>
</tr>

</table>


### Table of Contents

- [Project Overview](#project-overview)
- [Key Contributions](#key-contributions)
  - [1. DQN Implementation](#1-dqn-implementation)
  - [2. Reward System Development](#2-reward-system-development)
  - [3. Project Crisis Management](#3-project-crisis-management)
  - [4. Hyperparameter Tuning](#4-hyperparameter-tuning)
  - [5. Overall Project Management](#5-overall-project-management)
- [Additional Resources](#additional-resources)
- [Collaboration and New Perspectives: Keys to Breakthroughs](#collaboration-and-new-perspectives-keys-to-breakthroughs)

## Project Overview

<p align="center"><img src="https://github.com/user-attachments/assets/2c673807-6d79-46e5-9b6b-5c09117d8254" width="70%" height="70%"></p>

The project addressed a corporate challenge:  
Develop an autonomous agent (O, 1-month-old) utilizing reinforcement learning to efficiently collect designated items and return to the starting point while navigating around obstacles.

Our approach paralleled child development principles — implementing positive reinforcement (🧡💛💛💚💙💜) for desired behaviors and corrective feedback (🤬🤬🤬🤬🤬) for suboptimal actions. ~~Parenting is indeed challenging...~~

# Key Contributions

## 1. DQN Implementation
I implemented and experimented with Deep Q-Network (DQN) for this project.

Initial discussions encompassed various approaches, from heuristic methods to state-of-the-art RL models. Given the environment's constraints and task specifications, my team strategically chose to focus on fundamental reinforcement learning models that ensured comprehensive understanding among all team members.

### Understanding DQN

DQN approximates the action-value table (Q-Table) using a neural network function Qθ(s, a).  
The Q-function outputs the expected value given a state and an action — effectively estimating the optimal action value in any given state.

> Consider having an advisor named Q providing guidance for each move in a game. Initially, Q's decision-making capabilities are suboptimal compared to human performance.  
> The reinforcement learning process involves systematic feedback: negative reinforcement for unsuccessful outcomes and positive reinforcement for successful ones, gradually elevating Q to expert-level performance.

---

## 2. Reward System Development

<p align="center"><img src="https://github.com/user-attachments/assets/10f6416c-3d0e-4711-9acb-7ba8491780b9" width="70%" height="70%"></p>

The initial reward system had simple values: movement (+0.1), obstacle interaction (+0.1), and goal achievement (+10).  
This led to the agent wandering without pursuing items.

This observation led me to design a new reward system based on the agent's distance from items.

<table align='center'>  
<tr>
<td>
<div>
<img src="https://github.com/user-attachments/assets/f4e2bdce-881d-45fd-8e27-144e49e14007" />

</div>
</td>
<td>
<div>
<img src="https://github.com/user-attachments/assets/d112dd25-550f-4f44-aaac-339af61c628d" />
</div>
</td>
</tr>

</table>

I redesigned the reward system with the following structure:

- Item-directed movement: positive reward
- Movement away from items: penalty
- Cumulative rewards scaled with proximity to items

Result: The agent successfully pursued items as intended. 😎

---

## 3. Project Crisis Management

- With only two weeks remaining and no model convergence, team members were on the verge of giving up
- As team leader, proposed a final discussion to share our individual attempts
- Led a meeting to share experimental results and insights
- Maintained team motivation and redistributed roles effectively


## 4. Hyperparameter Tuning

- Orchestrated parallel model experiments on Google Cloud Platform (GCP)
- Implemented systematic hyperparameter optimization through iterative experimentation
- Maintained comprehensive experimental documentation on Padlet

---

## 5. Overall Project Management

The project spanned 1.5 months, encompassing:
- Accelerated reinforcement learning curriculum completion (1 week)
- Implementation of structured study sessions with targeted Q&A
- Development of comprehensive GitHub workflow documentation
- Systematic project tracking through Notion and Padlet

---

# Additional Resources

- [Original Project Repository](https://github.com/O-GangZa)
- [Comprehensive Project Documentation](https://docs.google.com/presentation/d/1g4rSnndIC1UPRLtctxpKDnUgFjEsVCXwA8oUc9TbBMQ/edit?usp=sharing)
- [Project Management Dashboard](https://www.notion.so/f47ef3d55d86420985d99491af2fdd76?pvs=21)
- [Learning Progress Documentation](https://padlet.com/tmsk0711/ogangza)
- [Hyperparameter Optimization Records](https://padlet.com/tmsk0711/ogangza_parametertuning)  
~~Sorry, Most of them are written in Korean, But there are good tool - Translation tool.~~

We appreciate your interest in our dedicated efforts!

# Collaboration and New Perspectives: Keys to Breakthroughs

Through this project, I gained two key insights: the synergy created through collaboration and the importance of approaching problems from multiple perspectives.

With only two weeks remaining until the deadline and no progress in model performance, some team members began to suggest giving up. Although I also felt discouraged, as the team leader, I decided to reassess the situation. Each member had been experimenting independently, so I organised a meeting to share our approaches and results. By identifying which methods to improve, discard, or pursue, we clarified our next steps and reallocated roles. As a result, we achieved model convergence within just one week.

This experience taught me that collaboration can create outcomes that would have been impossible to achieve alone.

I also learned that viewing problems differently can lead to breakthroughs. I have applied this lesson ever since. For example, in a poultry defect detection project, we struggled to detect bruises due to dark, flash-lit data. Searching for alternatives, I discovered that forensic science uses UV light to examine bruises, which inspired me to propose a new detection approach.




