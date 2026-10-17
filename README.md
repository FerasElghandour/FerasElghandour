# Feras Elghandour

### AI Research Engineer | Deep Learning & Autonomous Systems

I develop, train and evaluate machine-learning models, from neural architectures and generative models to reinforcement-learning policies. I focus on how models learn and how their behavior holds up under evaluation.

[Portfolio](https://feraselghandour.github.io/) · [LinkedIn](https://www.linkedin.com/in/feras-elghandour/)

## Selected work

Six projects in model training, generative learning, control and AI systems. Figures show recorded results; project documentation explains the method, contribution and evaluation scope.

### 01 · [Recursive Network Capacity Study](https://github.com/FerasElghandour/recursive-network-capacity-study)

**Does network topology change what a model learns?** Train balanced, random and skewed recursive networks against dense models. Compare four datasets, feature orders and compute budgets.

[![Four recorded accuracy plots compare balanced, random and skewed trees with a dense MLP across model sizes.](https://raw.githubusercontent.com/FerasElghandour/FerasElghandour.github.io/main/assets/capacity-results.png)](https://github.com/FerasElghandour/recursive-network-capacity-study)

1,120 recorded experiments. Balanced trees beat random trees in 14 of 16 native settings, but the corrected-compute dense comparator in only 5 of 16. Dense models remain faster.

<sub>Actual study figure: test accuracy against trainable parameters. Lines show means; bands show one seed standard deviation across ten seeds. Native feature order.</sub>

[Interactive evidence report](https://feraselghandour.github.io/recursive-network-capacity-study/) · [Source code](https://github.com/FerasElghandour/recursive-network-capacity-study)

### 02 · [Shared-Policy DDPG: Tennis](https://github.com/FerasElghandour/tennis-reinforcement-learning)

**Learn a continuous control policy.** Train a shared actor–critic policy with replay, target updates and bounded continuous actions. Package the saved policy for CPU inference.

[![Recorded rolling 100-episode Tennis training score rises, peaks, then falls before a partial recovery.](https://raw.githubusercontent.com/FerasElghandour/FerasElghandour.github.io/main/assets/tennis-report.png)](https://github.com/FerasElghandour/tennis-reinforcement-learning)

The saved policy averages 2.067 over 100 historical evaluation episodes. The recorded training trace shows learning progress, variability and later regression.

<sub>Actual recorded training curve: the rolling 100-episode mean across 875 training episodes. This is a separate record from saved-policy evaluation. One training seed.</sub>

[Interactive evidence report](https://feraselghandour.github.io/tennis-reinforcement-learning/) · [Source code](https://github.com/FerasElghandour/tennis-reinforcement-learning)

### 03 · [VAE and Beta-VAE Comparison](https://github.com/FerasElghandour/tabular-vae-comparison)

**Measure the cost of stronger regularization.** Train a 30-feature VAE with a two-dimensional latent space. Compare β = 1 and β = 4 using training-only scaling and deterministic mean-latent reconstruction.

[![VAE test reconstruction MSE is 0.2831 for beta one and 0.3231 for beta four.](https://raw.githubusercontent.com/FerasElghandour/FerasElghandour.github.io/main/assets/vae-comparison.png)](https://github.com/FerasElghandour/tabular-vae-comparison)

Recorded test reconstruction MSE: 0.2831 at β = 1 and 0.3231 at β = 4. Stronger regularization increases reconstruction error in this experiment.

<sub>Replotted from results/reproduction.json, October 17, 2026. Lower test reconstruction MSE is better. A small benchmark experiment, with no clinical or privacy guarantee.</sub>

[Implementation and evaluation](https://github.com/FerasElghandour/tabular-vae-comparison) · [Source code](https://github.com/FerasElghandour/tabular-vae-comparison)

### 04 · [Autonomous Braking Simulation](https://github.com/FerasElghandour/autonomous-braking-simulation)

**Connect sensing to a measurable stop.** Build a Webots controller that validates sensing, computes time to collision and enters a persistent braking state. Check the run with an independent supervisor.

[![Ground-truth speed and obstacle distance over the recorded 17-second braking simulation.](https://raw.githubusercontent.com/FerasElghandour/FerasElghandour.github.io/main/assets/braking-telemetry.png)](https://github.com/FerasElghandour/autonomous-braking-simulation)

The recorded static-obstacle run lasts 17.056 seconds without collision, with a minimum ground-truth obstacle distance of 15.3837 metres.

<sub>Replotted from the saved run.csv. Dashed line marks entry into the braking state. Simulation evidence from one straight-road, static-obstacle scenario.</sub>

<a href="https://github.com/FerasElghandour/autonomous-braking-simulation"><img src="https://raw.githubusercontent.com/FerasElghandour/autonomous-braking-simulation/main/results/final_screenshot.png" alt="Actual Webots frame from the recorded braking simulation" width="480"></a>

<sub>Actual simulator frame from the recorded run. Simulation, rather than physical-vehicle deployment.</sub>

[Implementation and evaluation](https://github.com/FerasElghandour/autonomous-braking-simulation) · [Source code](https://github.com/FerasElghandour/autonomous-braking-simulation)

### 05 · [Sensor Fusion Policy Engine](https://github.com/FerasElghandour/sensor-fusion-policy-engine)

**Govern what reaches the fusion decision.** Apply versioned camera/radar release policies before association and persistence. Compare a deterministic matcher with a learned scorer while retaining decision provenance.

[![Deterministic sensor association has mean F1 0.9416; learned association has mean F1 0.9298 across three seeds.](https://raw.githubusercontent.com/FerasElghandour/FerasElghandour.github.io/main/assets/fusion-comparison.png)](https://github.com/FerasElghandour/sensor-fusion-policy-engine)

Across 3,000 synthetic missions, mean association F1 is 0.9416 for the deterministic method and 0.9298 for the learned method.

<sub>Replotted from the recorded three-seed release evaluation. Each dot is one seed. Results describe synthetic missions, rather than operational sensor performance.</sub>

[Interactive evidence report](https://feraselghandour.github.io/sensor-fusion-policy-engine/) · [Source code](https://github.com/FerasElghandour/sensor-fusion-policy-engine)

### 06 · [Predictive Maintenance](https://github.com/FerasElghandour/predictive-maintenance)

**Turn a prediction into a warning policy.** Build causal sensor features, compare Ridge and random-forest baselines, then select a maintenance threshold on validation engines before replaying test histories.

[![Observed test outcomes: 29 timely warnings, one early intervention, five misses and 65 censored engine histories.](https://raw.githubusercontent.com/FerasElghandour/FerasElghandour.github.io/main/assets/maintenance-outcomes.png)](https://github.com/FerasElghandour/predictive-maintenance)

Of 100 truncated historical test histories, 35 enter the observed danger window. Five of those receive no warning; 65 histories end before that window.

<sub>Replotted from the corrected report data. Categories sum to 100 test engines. The 45% health threshold was selected on validation; endpoint MAE is 13.44 cycles.</sub>

[Interactive evidence report](https://feraselghandour.github.io/predictive-maintenance/) · [Source code](https://github.com/FerasElghandour/predictive-maintenance)

[Figure sources and context](https://github.com/FerasElghandour/FerasElghandour.github.io/blob/main/assets/FIGURE_SOURCES.md)

## Model development and training

- **Deep learning:** [CNN comparisons](https://github.com/FerasElghandour/handwritten-digit-cnn-comparison), [CIFAR-10](https://github.com/FerasElghandour/cifar10-convolutional-classifier), [landmark classification](https://github.com/FerasElghandour/landmark-cnn-architecture) and [transformer sentiment classification](https://github.com/FerasElghandour/sentiment-transformer-architecture).
- **Generative AI:** [GAN and diffusion experiments](https://github.com/FerasElghandour/conditional-handwriting-generation), [VAEs](https://github.com/FerasElghandour/tabular-vae-comparison) and [LoRA/GRPO adaptation](https://github.com/FerasElghandour/llm-counting-reward-design).
- **Reinforcement learning:** [shared-policy DDPG](https://github.com/FerasElghandour/tennis-reinforcement-learning), [continuous control](https://github.com/FerasElghandour/continuous-control-ddpg) and [Double DQN](https://github.com/FerasElghandour/navigation-double-dqn).
- **Experimental research:** [neural architecture capacity](https://github.com/FerasElghandour/recursive-network-capacity-study), [compositional generalization](https://github.com/FerasElghandour/recursive-composition-benchmark) and [forecasting evaluation](https://github.com/FerasElghandour/forecasting-replay-lab).

## Autonomous systems, safety and delivery

I connect simulated vehicle control, learned continuous policies and camera/radar processing prototypes. Physical AI, robot learning and reliable autonomy are research directions, building on current simulation and prototype work.

My AI safety research includes two first-author EuroMed 2026 conference papers on autonomous-system safety frameworks and AI coherence metrics. [Proceedings](https://euromedacademy.org/publications/conference-book-of-proceedings/volume-19/).

My commercial background adds experience in requirements, economics, workflow adoption and delivery coordination. [Client case studies](https://feraselghandour.github.io/#client-work) describe selected engagements and documented outcomes.

Projects include independent research, coursework and engineering prototypes, with course materials, upstream work and AI assistance attributed where applicable. Documentation distinguishes historical experiments, public component editions and the results reproduced by available checks.
