# Hvla_manipulation_robustness

## Motivation
We consider Vision-Language-Action (VLA) models are designed to be more general and flexible, especially for serving humans in real-world environments. In everyday scenarios, robots do not always start from a fixed or standard initial position. The robot’s pose, orientation, and object placement may vary significantly. This motivates our project: we want to test whether a hierarchical VLA system can still perform well when the robot starts from different initial conditions.
## Brief related work
- Wang, Z., Li, Y., Xie, A., Zhang, Y., & Gupta, A. (2024). HAMSTER: Hierarchical action models for open-world robot manipulation. arXiv preprint arXiv:2502.05485 
- Gemini robotics
- DePi
## Research problem statement and hypothesis
We aim to investigate:
To what extent can a hierarchical VLA model maintain coherent reasoning and task performance under progressively stronger shifts in spatial initial conditions? Specifically, we vary the robot’s Initial pose / Orientation / Relative object layout, rather than keeping initial states near training distributions.
## Proposed approach
We design two experimental scenarios to compare two VLA architectures under spatial distribution shift.
Scenario1 : Monolithic VLA
We use the Depi policy as a representative monolithic VLA model.
Scenario2 : Hierarchical VLA
- High-Level Policy:
 We will use HAMSTER-style hierarchical VLM architecture ,specifically we will use Gemini Robotics API, and then evaluate zero-shot reasoning performance.
- Low-Level Policy: 
We will incorporate a model-based control module (e.g., MPC) for low-level execution..
