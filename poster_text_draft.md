# Overview:

Network science and cognitive science are two approaches to explaining social diffusion dynamics.

- Network Science:
    - How individuals are connected to other individuals
    - Network topology
    - Diffusion is a function of an individual's connected neighbors
- Cognitive Science:
    - How an individuals process information from external input
    - Model of an individual
    - Diffusion is a function of how individuals process inputs

We developed a simulation platform to combine network science and cognitive science to explore
social diffusion dynamics using a **networked cognitive systems approach**.


# Multi-Agent Neural-Network (MANN)

- Agent-based modeling platform built in Python
- Networks are created with networkx
- Neural networks are created in using LENS (Light, efficient simulator)
- Open Source

# Compartmental Models -> Agent-Based Models

## Compartmental Models

S -infectious/day-> I -recovered/day-> R
dS/dt = -bS(t)I(t)
dI/dt = bS(t)I(t) - kI(t)
dR/dt = kI(t)

- Relatively simple
- Deterministic
- Overall System Dynamics
- Homogeneous

## Agent-Based Models

abm_segration_image

abm_wolf_sheep_image

abm_virus_network_image

- Stochastic
- Consolidate knowledge for agent rules
- Heterogeneous

picasso_lithograph_image

# Binary Decisions with Externalities

- Network science approach
- ABM where agents (individuals) are connected to one another
    - Random
    - Small-world
- Each agent has a binary outcome
    - Local dependencies - connected neighbors that are different
    - Fractional threshold - proportion of neighbors different
    - Heterogeneous
- Look for information flow through network (global cascades)
- Simple model that can be used to explain multiple phenomena
    - fads, riots, crime, competing technologies, spread of innovation, conventions, and cooperation

| Degree (k) | Threshold ($\phi$) | Vulnerability |
|------------|--------------------|---------------|
| High       | High               | Low           |
| High       | Low                | High          |
| Low        | High               | Low           |
| Low        | Low                | High          |

Watts 2002 Figure 1

mann2_watts_figure

# Expanding the Watts model

In cognitive science, artificial neural networks have been used to model how humans process information.
Decisions, and similarly, behaviors, are binary, but the process of making a decision and performing an action is not.

Neural networks allow us to use multi-dimensional agents, not just a simple binary agent.

## Theory of Reasoned Action

- Health behavior model
- Martin Fishbein and Icek Ajzen 1967
    - Behavior is determined by an individual’s intention
    - Intention comes from an individual’s attitudes and social context
    - Attitudes and social context originates from a set of beliefs

beliefs → (attitudes & social context) → intention → behavior

## Auto Associative Neural Network

- learn and reproduce an identity (a.k.a, prototype) given a portion of inputs
    - "Jack and Jill ..."
    - "So long and thanks for all the ..."
    - "Answer to the Ultimate Question of Life, the Universe, and Everything

We parameterize the TRA with neural networks

Orr 2014 Figure 1
Orr 2013 Figure 1
Orr 2013 Figure 2

2014-12-06 email with mark image

# Research Questions

1. How do we measure if information has been passed from one node to another?
1. How do we map fractional thresholds between the two models?
1. How do we provide inputs to nodes that have been designated to carry and propagate information in the network?

mann1 individual signals over time image

An approach would be to have each node in the network trained against the prototype.
Seed a single node with the prototype, and run the model without any additional thresholding rule ($\theta$),
and have each node use a random 1 neighbor's state (i.e., output) and its input.

Forthcoming Publication
parameter sweep on NN
connections
• no learning during simulation
• 7750 Simulations
• associativity
clustering of intention at the
end of the simulation

Assorsitivity image

# Refactoring

mann2 class diagrams

# Future Directions

- summarize the neural network simulation data
- t-SNE projections over time to look for community movement