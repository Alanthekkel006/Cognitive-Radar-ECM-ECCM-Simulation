# Cognitive Radar Electronic Warfare: Inverse Learning & ECCM Simulator

A Python-based simulation modeling a complete cognitive radar loop (Sense → Learn → Adapt), designed for edge-hardware deployment.

## Architecture Breakdown:
* **Data Generation:** Mathematical synthesis of Spot, Sweep, and Barrage Electronic Countermeasures (ECM) with heavy thermal noise and signal fading.
* **Sense (Inverse Learning):** A hybrid Conv1D-LSTM-Attention network that processes noisy time-series RF data to classify the adversary's hidden jamming strategy in real-time.
* **Adapt (ECCM Engine):** A Deep Q-Network (DQN) Reinforcement Learning agent that utilizes the classified threat state to autonomously discover optimal frequency-hopping evasion policies via the Bellman equation, bypassing rigid Game AI heuristics.

## Benchmarks
After 500 episodes of training, the DQN agent consistently achieves a >95% evasion survival rate against sweeping jammers, successfully breaking past the 80% baseline of legacy fixed and random-hopping radar systems.
