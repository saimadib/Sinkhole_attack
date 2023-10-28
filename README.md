# Sinkhole Attack Simulation in DODAG Network

## Overview

This project simulates the impact of sinkhole attacks in a Destination-Oriented Directed Acyclic Graph (DODAG) network. Sinkhole attacks involve malicious nodes that divert, intercept, or drop network traffic, affecting the network's performance and reliability. This repository contains code and results for different scenarios with varying numbers of malicious nodes.


## Contents

- [Prerequisites](#prerequisites)
- [Project Structure](#project-structure)
- [Usage](#usage)
- [Results and Observations](#results-and-observations)
- [Contributing](#contributing)

## Prerequisites

Before running the simulation, ensure you have the following prerequisites:

- Python environment (version 3.9)

## Project Structure

- `DODAG simulation.py`: The main simulation script for the Destination-Oriented Directed Acyclic Graph (DODAG) network without malicious nodes.
- `DODAG_sinkhole simulation.py`: The main simulation script for Destination-Oriented Directed Acyclic Graph (DODAG) network with malicious nodes.
- `results/`: Directory containing results and logs.

## Usage

1. Clone the repository to your local machine:

2. Run the simulation with different scenarios by modifying the code or input parameters.

3. View the results and log files to analyze the impact of malicious nodes on the network.

## Results and Observations

### Scenario 1: No Malicious Nodes

- In a healthy network without malicious nodes, all packets are successfully delivered to the root node.

- The overall delivery ratio is 100%, indicating that all messages reach their intended destination.

- The propagation delay is equal to the total number of messages (1000ms in this case).

### Scenario 2: 3 Malicious Nodes

- The network consisted of 10 nodes, generating a total of 1000 packets. 

- The results showed that only 101 packets were delivered to the root node, resulting in an overall delivery ratio of 10.1%. 

- Nodes 3 and 7 were the only nodes that successfully received and forwarded packets, while nodes 2 and 9 maliciously dropped all the packets they received.



### Scenario 3: 5 Malicious Nodes

- The network consisted of 50 nodes, generating a total of 1000 packets.
  
- Node 3, 15, 23, 36, and 48 are malicious nodes with a packet dropping ratio of 100%.

- The overall_delivery_ratio is 51.9%.



### Scenario 4: 12 Malicious Nodes

- With 12 malicious nodes, the behavior of the network is highly disrupted, as these nodes intentionally drop packets, affecting the communication between nodes.

- We can see that nodes 2, 8, 16, 21, 28, 35, 46, 57, 58, 65, 73, and 82 are the malicious ones, as their packet dropping ratio is 100.0%. 

- Nodes 11, 12, 16, 21, 28, 35, 46, and 57 did not receive any packets, which suggests that they might be isolated from the network, as the malicious nodes could have dropped all their packets.

- The overall_delivery_ratio is 3.1%. 

![result](https://github.com/saimadib/Sinkhole_attack/assets/88191474/a14952c3-f5c8-4904-8606-88affa9fc569)

## Contributing

Contributions are welcome! If you'd like to improve the project or add new features, please fork the repository and create a pull request. Feel free to open issues for any questions or suggestions.

