# SIR Model Simulation (Python)

# Overview

This project simulates the spread of an infectious disease using the SIR (Susceptible–Infected–Recovered) model on a 2D grid.

Each cell represents an individual, and the infection spreads to neighboring cells based on probabilistic rules. The simulation visualizes both:
	•Time evolution of S, I, R ratios (graph)
	•Spatial spread of infection (animation)


# Features
	•Grid-based SIR simulation (cellular automaton style)
	•Probabilistic infection and recovery
	•CSV output of S/I/R ratios over time
	•Graph visualization using matplotlib
	•Animated visualization of infection spread (GIF)


# Model Description
Each cell can be in one of three states:
	•S (Susceptible)
	•I (Infected)
	•R (Recovered)

Transition rules:
	•S → I (infection)
        Depends on the number of infected neighbors:
        P(infection) = 1 - (1 - β) ^ n
        where:
	    •β = infection rate
	    •n = number of infected neighbors
	
    •I → R (recovery)
        Occurs with probability γ
	
    •R → R
        Remains recovered


# Parameters
