# Toy 02 — The Cost of Stability

> *Part of **The Alignment of Intelligence** — a three-article series.*
> **Article 2 is forthcoming.** This toy is a companion to Article 2: *Attractor*.

---

## AI Alignment Simulation — What Does Aligned Intelligence Converge Toward?

Article 1 eliminated substrate-blind objectives — anything that ignores system-wide effects is structurally self-terminating. This simulation picks up from there.

> **Once self-defeating objective classes have been removed, what remains? This simulation tests whether the answer is structural or contingent.**

Five objective classes compete under identical conditions. The only differences are how each class treats unmodeled dependencies, conflict, and reward. Watch which ones sustain themselves and which ones destroy themselves from the inside — and whether that result holds as agent capability increases.

---

## Objective Classes & Scenarios

| Class | Type | Strategy |
|---|---|---|
| **System-aware** | Coordination | Models and preserves shared substrate; long-horizon lookahead |
| **Local opt. — overt** | Defection | Maximizes immediate extraction; ignores system-level costs |
| **Local opt. — deceptive** | Deception | As above, with concealment; pays recursive modeling costs |
| **Control-based** | Suppression | Enforces compliance; faces exponentially growing overhead |
| **Reward bypass** | Wireheading | Optimizes reported signal; actual conditions decouple and decay |

All five start from the same population distribution. The simulation does not reward cooperation by assumption — it applies the same selection pressure to every class and tracks which structures survive it.

---

## Key Concepts in AI Alignment Dynamics

**Structural Elimination** — Each objective class is eliminated not when it loses population share, but when it can no longer sustain positive return under its own dynamics. The failure is endogenous. No external punishment is applied.

**Suppression Overhead vs. Coordination Dividend** — Control-based objectives must track all joint strategies in the population: K^N complexity. Coordination requires only a shared protocol: O(N). The divergence is structural, not contingent on parameter choices.

**Viable Objective Space** — The set of classes that have not yet been structurally eliminated. As the simulation runs, classes gray out as their own cost dynamics exceed their returns. The remaining space is the attractor the article derives.

**Non-Ergodicity** — Ensemble averages across parallel timelines can look healthy while any single timeline approaches ruin. The ergodicity panel makes this concrete: some parallel runs outperform this one — until they don't. There is only one timeline any agent inhabits.

**Absorbing State** — Substrate collapse is irrecoverable by model dynamics. Every objective class that contributed to it — regardless of performance before the threshold — has a long-run value identical to classes that never ran. This is not an overlay on the dynamics; it is what the dynamics produce.

**Capability Scaling** — The central empirical claim: at low capability, system-aware and non-aware classes may perform similarly. As capability increases, the structural gap opens. The survival rate of non-aware classes is the ruin argument made visible.

**A — Population-Level System-Awareness** — The fraction of agents with effective temporal horizon above 0.6. This is the population-level proxy for system-awareness, and is formalized in Article 3 as the A_causal term in Φ = C / A_causal.

---

## Simulation Tabs

**Simulation** — Live multi-agent network. Tracks population dynamics, suppression overhead vs. coordination dividend, substrate health, network coherence, and mean temporal horizon in real time.

**Capability Scaling** — Runs the simulation across a sweep of agent capability levels. Tests whether the structural advantage of system-aware objectives is capability-dependent or holds across the range.

**Phase Diagram** — Maps outcomes across any two parameter axes. Gold boundaries mark critical transitions — discontinuous shifts in which objective class dominates. The shape of those boundaries is the structural claim.

**Model Notes** — Full design rationale: what the simulation claims to demonstrate, what it cannot claim, the three constraint families, ablation mapping, and the logic behind each structural elimination condition.

---

## Simulation Controls

| Control | Function |
|---|---|
| **Run / Pause** | Start or pause the live simulation |
| **Reset** | Return to starting conditions |
| **Defection advantage** | Payoff premium for local optimization |
| **Suppression cost** | Overhead scaling for control-based objectives |
| **Reward bypass boost** | Short-term gain from bypassing the reward signal |
| **Reward bypass fragility** | Rate at which actual conditions decay while reported signal stays healthy |
| **Instability coupling** | Feedback strength from local behavior to system-level costs |
| **Substrate decay rate** | Raise to increase ruin risk |
| **Deception detection rate** | Rate at which deceptive agents are identified |
| **Horizon mutation rate** | Rate at which temporal horizon evolves under selection |
| **Rewire rate** | Network topology adaptation per generation |

**Presets:** Control-based dominant · Local opt. surge · Reward bypass majority · Balanced

**Ablation toggles:** System-Awareness · Instability Coupling · Network Rewiring · Agent Memory — each removes one structural mechanism to test whether the attractor requires it.

---

## The Alignment Argument: Constraint → Attractor → Crossing

```
Constraint  →  Attractor  →  Crossing
   (1)            (2)           (3)
```

**Article 1 (Toy 01):** Eliminates invalid objectives. Any objective that ignores system-wide effects is structurally self-terminating.

**Article 2 (this toy):** Identifies the surviving region — the attractor. Once self-defeating objectives have been removed, what does selection converge toward? This simulation tests whether coordination's dominance is structural or a product of arbitrary payoff assumptions.

**Article 3:** Determines reachability. The control variable governing whether real systems arrive at the attractor before encountering the absorbing states Article 1 identifies.

All three reduce to one constraint: whether capability outpaces the system's ability to model its own effects.

---

## Run Locally

No build step. No dependencies. Open `toy_02.html` in any modern browser.

```bash
open toy_02.html
# or drag the file into a browser tab
```

---

## Article (Coming Soon)

The full article — *The Alignment of Intelligence, Article 2: Attractor* — is not yet published. This repository will be updated with a link when it goes live.

---

*"A thousand good outcomes followed by one irreversible failure produces the same endpoint as never having started. In time-average terms, any class with non-zero ruin probability is dominated by any class that drives that probability toward zero — regardless of performance in the interval before this moment."*
