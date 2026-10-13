# RTCP Manager

A formal modeling and verification project for **RTP/RTCP communication using UPPAAL**. The project models a real-time communication session between a sender and a receiver, including RTCP session management and attacker scenarios.

## Overview

The project explores how RTP communication and RTCP session management behave under normal and potentially malicious conditions. Using timed automata, the models represent communication states, packet exchanges, session closure, and timeout behavior.

The goal is to study the communication protocol and investigate how attacker behavior can affect a session through formal modeling and verification.

## Features

- **RTP communication modeling** — represents the exchange of RTP packets between a sender and a receiver.
- **RTCP session management** — models session lifecycle events, including session initialization and termination using RTCP BYE.
- **Timed behavior** — includes packet timing, RTCP intervals, and receiver session timeouts.
- **Attacker scenarios** — provides separate models for investigating attacker behavior during RTP communication.
- **Formal verification** — uses UPPAAL to analyze system states, transitions, timing constraints, and specified verification properties.


## Technologies

- **UPPAAL** — modeling and verification of timed automata.
- **RTP (Real-time Transport Protocol)** — real-time media packet transmission.
- **RTCP (RTP Control Protocol)** — session control and communication monitoring.
- **Formal methods** — analysis of system behavior, timing constraints, and security-related scenarios.

## Getting Started

### 1. Install UPPAAL

Download and install UPPAAL from the official website:

https://uppaal.org/

### 2. Clone the repository

```bash
git clone https://github.com/moeC4070/RTCP_Manager.git
cd RTCP_Manager
```

### 3. Open a model

Launch UPPAAL and open one of the XML files:

- `RTP.xml` for the baseline communication model.
- `RTP_Attacker.xml` for the first attacker scenario.
- `RTP_ImplAttacker.xml` for the alternative attacker scenario.

### 4. Simulate and verify

Use UPPAAL's **Simulator** to explore the automata, inspect transitions, and observe how the system evolves over time.

Use the **Verifier** to evaluate the verification queries defined in each model. Review the results to understand whether the specified properties hold.

## Model Overview

The baseline model includes the following components:

- **Sender:** initiates a session and transmits RTP packets.
- **Receiver:** accepts packets, tracks the session, and handles termination or timeout.
- **RTCP Manager:** models control-related behavior and timing associated with the communication session.

The models use timed automata and synchronization channels to represent interactions between components.

## Project Objectives

1. Model RTP communication and RTCP session management.
2. Understand the interactions between communicating components.
3. Investigate attacker-related scenarios.
4. Analyze protocol behavior through simulation and formal verification.
5. Identify potential weaknesses or violations of specified system properties.

## References

- [UPPAAL — Official Website](https://uppaal.org/)
- [RFC 3550 — RTP: A Transport Protocol for Real-Time Applications](https://www.rfc-editor.org/rfc/rfc3550)
