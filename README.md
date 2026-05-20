# Demand-Responsive Electric Vehicle Routing Under Uncertainty

## Overview

This project investigates routing optimization for demand-responsive electric mobility systems under uncertain customer demand.

A baseline vehicle routing model is implemented using Google OR-Tools and evaluated under electric vehicle battery constraints. Since the baseline route is optimized for distance without considering energy limitations, it may be infeasible in an electric vehicle setting.

To address this issue, the project implements a charging-aware route repair heuristic that dynamically inserts charging stops when the vehicle cannot safely continue the route.

## Research Question

Can a simple charging-aware route repair heuristic improve the feasibility of electric vehicle routes under uncertain demand?

## Problem Setting

The project considers a synthetic mobility network consisting of:

- A depot
- A charging station
- A set of customer locations
- Multiple demand scenarios where only a subset of customers is active

The vehicle must start and end at the depot while visiting all active customers.

## Methodology

The project consists of four main steps:

1. Generate a synthetic mobility network.
2. Solve a baseline routing problem using OR-Tools.
3. Evaluate route feasibility under battery constraints.
4. Apply a charging-aware repair heuristic that inserts charging stops when needed.

## Key Findings

- Baseline routes optimized without battery constraints can be infeasible for electric vehicles.
- The charging-aware repair heuristic restores feasibility across all tested demand scenarios.
- Feasibility improvement comes at the cost of longer routes due to additional charging detours.
- Demand uncertainty affects route structure, energy requirements, and charging needs.

## Report

The full project report is available here:

[ev_routing_under_uncertainty_report.pdf](ev_routing_under_uncertainty_report.pdf)

## Repository Structure

```text
ev_routing_under_uncertainty.ipynb       Jupyter notebook with the routing experiment
ev_routing_under_uncertainty_report.pdf  Project report
requirements.txt                         Python dependencies
README.md                                Project description
