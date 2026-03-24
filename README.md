# The Cost of Stability

A multi-agent network simulation built as a companion to the article **What does aligned intelligence actually converge toward?** *(link to be added when published on Medium)*

## What this demonstrates

The companion article argues that once the structural constraint identified in [The Alignment of Intelligence](https://medium.com/@diamondlight/the-alignment-of-intelligence-8410069f2517) is satisfied, optimization does not converge arbitrarily — it converges toward a specific shape. The direction is constrained by the structure of the environment, and that constraint is strong enough to be partially derived.

This simulation tests that claim. The central question: does system-awareness become instrumentally necessary as optimization capability increases? Or does it only happen to win under specific parameter choices?

## How to run it

Open `cost_of_stability_v5.html` in any modern browser. No installation, no dependencies.

*(Live URL to be added when deployed to GitHub Pages)*

## What's in the simulation

**Simulation tab** — 110 agents on a small-world network. Five behavioral types: cooperative (with continuous temporal horizon parameter), defecting, deceptive defecting, suppressive, and wireheading. Watch the population dynamics, substrate health, network coherence, and mean temporal horizon evolve in real time.

**Capability Scaling tab** — The decisive experiment. Sweeps across mean agent capability levels and measures whether long-horizon agents displace non-aware agents as capability increases — and whether non-aware agent survival rates drop at high capability (the ruin argument made visible in selection dynamics).

**Phase Diagram tab** — Runs headless mini-simulations across pairs of parameters and maps where the cooperative attractor holds and where it breaks down. Gold lines mark critical transition boundaries. Wide blue = robust attractor. Narrow = assumption-sensitive.

**Model Notes tab** — Explains what the simulation claims to demonstrate, what it cannot claim, how the ablation toggles map to the three constraint families the article identifies, and why the gap between selection dynamics and optimizer convergence remains the central open question.

## Key features

- **All payoff assumptions exposed as sliders** — cooperation gain, defection advantage, suppression order bonus, instability coupling, substrate decay rate. The attractor should hold across a wide range. If it doesn't under your parameter choices, that's information.
- **Ablation panel** — disable system-awareness, instability coupling, network rewiring, or memory independently to isolate which mechanisms are doing the work
- **Substrate decay** — payoffs scale with system health; defection and suppression erode it; coordination restores it
- **Dynamic rewiring** — agents drop low-payoff connections and seek high-payoff neighbors; cooperative clusters form structurally
- **Deceptive defection** — agents that signal cooperation but extract defection payoffs; long-horizon agents detect them over time through payoff history tracking
- **Wireheading agents** — agents with split state (reported condition vs actual condition); they appear healthy while their actual conditions degrade

## What to look for

Run the **Capability Scaling** experiment first. Watch whether the survival rate of non-aware agents drops sharply at high capability while long-horizon agents maintain stable survival. If it does across a wide range of parameter settings, you are seeing the time-average dominance argument approximated in selection dynamics.

Then use the **ablation panel**. Turn off instability coupling and observe whether coordination still emerges. If it does, the payoff structure is doing the work, not the environmental feedback. Turn off system-awareness and observe whether suppression still collapses. If it does, the structural costs are accumulating regardless of what agents model.

Then run the **Phase Diagram** with defection advantage on one axis and instability coupling on the other. The shape of the boundary between cooperative and defection-dominant regions is itself a claim: sharp means tipping point, gradual means smooth parameter sensitivity.

## What this simulation cannot claim

This is a model of evolutionary selection dynamics, not of objective alignment under increasing optimization pressure. What evolves under selection is not necessarily what an optimizer with a fixed objective converges to. The simulation demonstrates that selection favors long-horizon, system-aware strategies. It does not demonstrate that a sufficiently capable optimizer will necessarily develop system-awareness.

That gap — between selection dynamics and optimizer convergence — is the central open question of the companion article. It is described in the Model Notes tab as a known open problem rather than a solved one.

## Part of a series

1. **[The Alignment of Intelligence simulation](https://github.com/bethediamond/alignment-model)** — demonstrates why misaligned optimization is structurally self-terminating
2. **This simulation** — demonstrates what aligned optimization converges toward, and tests whether system-awareness becomes necessary as capability scales

## The argument it illustrates

The three constraint families the article derives — ruin avoidance under dependency opacity, coordination dominance over suppression, and adaptive preference integrity — are approximated in this simulation. The ablation panel lets you test each independently. A [one-page formal sketch](https://github.com/bethediamond/cost-of-stability/blob/main/formal_sketch.md) converts these constraint families into mathematical objects that a theorist could attempt to formalize or refute.

## Feedback and critique

Readers are encouraged to vary the parameters and attempt to break the result. A result that fails to show the expected transition is not a broken simulation — it is information about which assumptions matter.

Critique, attempted refutations of the underlying argument, and formalization attempts are genuinely invited. The companion article issues that challenge directly.
