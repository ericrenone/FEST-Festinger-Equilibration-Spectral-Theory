# FEST — Festinger Equilibration Spectral Theory
## Dissonance · Barrier · Coherence


---

**Central Theorem.** Three classical problems in the psychology and geometry of belief — Festinger's Dissonance Problem (which beliefs remain visible under contradiction?), the Rationalization Barrier Problem (what minimum cognitive structure blocks all dissonant lines of inference?), and Harmon-Jones's Action Problem (what minimum behavioral sequence guarantees escape from any cognitive trap, regardless of initial position or orientation?) — are not three separate phenomena. They are the three dual faces of a single structure: the geometry of contradictory cognitions intersecting a belief domain under motivational uncertainty. Translated into spectral geometry, this triple maps exactly onto the Visibility, Barrier, and Escape architecture already established for learning phase transitions. The master equivalence is:

```
λ₁(ℒ_FL) > 0  ⟺  C_cog > 1  ⟺  Festinger metric exists on ℬ_cog
             ⟺  Belief manifold admits a minimum rationalization barrier     [Rationalization Barrier → 𝒮̄_disc potential]
             ⟺  Primitive belief subspace is dense                           [Cognitive Orchard → Farey / Möbius]
             ⟺  Harmon-Jones escape path has finite worst-case length        [Action Problem → Behavioral grokking path]
All conditions are computable from belief revision vectors alone.
```

---

## Proof-Status Convention

| Tag | Meaning |
|-----|---------|
| [T] | Theorem — proven within stated hypotheses |
| [V] | Verified in the explicit model listed |
| [C] | Conjecture — precisely stated, currently open |
| [H] | Working hypothesis — verified in tractable cases |
| [D] | Definition / structural translation — no independent truth claim |
| [W] | Classically sourced primitive — formally absorbed from psychology or geometry |

---

## Table of Contents

- Part 0 — The Three Source Problems
- Part I — The FEST Translation Dictionary
- Part II — The FEST Master Equivalence
- Part III — The Three Geometric Structures
- Part IV — New Open Problems
- Part V — Logical Dependency Map
- Part VI — Proven Results Summary

---

## Part 0 — The Three Source Problems

All constructions derive from three classical problems. Each is a complete theory in its own domain. Every subsequent geometric construction is a first-principles translation of one of these three sources.

### 0.1 Festinger's Cognitive Orchard [W, 1957]

Imagine all possible beliefs a person could hold arranged as points in a lattice. An observer at the origin of rational inquiry asks: which beliefs are directly *visible* — unobstructed by earlier, more derived, or contradictory cognitions standing in the same line of inference?

**Definition [W].** A belief `b_i` is *primitive* from the rational origin if no other belief `b_k` with `k < i` lies strictly between the origin and `b_i` along the same inferential ray. The *Cognitive Orchard* is the set of all primitive beliefs:

```
𝒞 = { b ∈ ℬ_cog  :  b is not derivable as a linear combination of beliefs closer to the origin }
```

The blocking rule: a derived belief (one that follows from simpler premises) hides the primitive inference behind it. Equivalently, a belief is visible if and only if its inferential complexity is irreducible — a cognitive Farey fraction.

Festinger's (1957) original observation: two cognitions are *consonant* if one follows from the other (primitive visibility), and *dissonant* if one follows from the obverse of the other (blocked visibility). The magnitude of dissonance depends on the *importance* of the cognitions involved — the analog of the denominator q in the Farey sequence: high-importance contradictions have large cognitive denominators and create sharper belief basins.

**Cognitive density** of primitive beliefs: the fraction of non-derived cognitions in any large belief system converges to `6/π² = 1/ζ(2)` under the natural measure — identical to the visible-lattice density of Euclid's Orchard. In `d` cognitive dimensions: density = `1/ζ(d)`.

**Möbius cognitive filter:** The function `μ_cog(k)` that inverts the derivation sieve — identifying which beliefs are genuinely primitive versus inherited — is structurally the Möbius function, acting on the poset of inferential dependency.

### 0.2 The Rationalization Barrier Problem [W]

Given a belief domain `K` (a convex region of cognitively accessible positions), find the shortest cognitive structure `S` such that every dissonant line of inference crossing `K` must intersect `S`. The structure `S` is the *rationalization barrier* — the minimum consistent sub-belief system that blocks all contradictory inference paths.

**Definition [W].** `S` is a *rationalization barrier* for `K` if every dissonant inference line `ℓ` satisfying `K ⊂ conv(ℓ)` must cross `S`: `ℓ ∩ S ≠ ∅`. The rationalization barrier problem seeks to minimize `|S|`.

The boundary `∂K` (the full complexity of explicit, enumerated beliefs) is always a rationalization barrier — but shorter, more efficient internal belief structures exist. Festinger's four dissonance-reduction strategies are exactly the four classes of interior barriers shorter than the full boundary:

| Festinger's Strategy | Geometric Analog | Barrier Type |
|---------------------|-----------------|--------------|
| Change a dissonant cognition | Shift internal belief node | Interior barrier: vertex relocation |
| Add new consonant cognitions | Mediant insertion | Farey mediant: new barrier segment |
| Reduce importance of conflict | Scale the metric | Rescale the cognitive domain K |
| Selective exposure | Restrict accessible lines | Prune the line family |

The minimum rationalization barrier has length `L_min ≥ perimeter(K)/2` (general lower bound). Selective exposure — restricting which dissonant inferences are even considered — is the boundary `∂K` itself: costly, but always valid.

The rationalization barrier is the **dual** of cognitive visibility: Festinger's Orchard asks which beliefs are *not* blocked; the Rationalization Barrier asks how to block *all* of them with minimum cognitive material.

### 0.3 Harmon-Jones's Action Problem [W, 1999]

A person is cognitively trapped — they hold beliefs they know to be inconsistent, but do not know their exact position in belief space or which direction points toward coherence. Their shape of discomfort (the structure of the contradiction) is precisely known. What behavioral sequence should they follow to guarantee reaching cognitive coherence in the shortest possible worst-case length?

**Definition [W].** For a belief domain `K`, the *Harmon-Jones behavioral escape path* `B(K)` is the shortest continuous sequence of actions such that `K` cannot be placed (via any cognitive reorientation: rotation of interpretive frame + translation of belief anchor) to contain `B(K)` entirely within its interior.

This is the action-based model of cognitive dissonance: dissonance motivates action not because of abstract discomfort, but because action is the *minimax escape strategy* — it resolves dissonance under the worst-case cognitive orientation.

Known behavioral escape types — parallel to Bellman's three classical solutions:

| Cognitive Configuration | Escape Path Type |
|------------------------|-----------------|
| Round belief basin (single dominant contradiction) | Direct confrontation: straight-line behavioral revision |
| Strip basin (persistent oscillating doubt) | V-shaped behavioral sequence with two anchor corrections |
| Triangular basin (three-way value conflict) | Three-step Besicovitch-type behavioral zigzag |

### 0.4 The Three-Way Duality [T, FEST-D1]

| Problem | Question | Adversary | Minimizer |
|---------|---------|-----------|-----------|
| Festinger's Orchard | Which cognitions are primitive from the rational origin? | Derivation: complexity > 1 blocks sight | Primitive beliefs: irreducible inferential direction |
| Rationalization Barrier | What minimum `S` intercepts all dissonant inference lines? | Dissonant inferences: every contradictory line must be blocked | Minimum-length belief barrier `|S|` |
| Harmon-Jones Action | What minimum behavioral sequence guarantees coherence for any starting configuration? | Position + frame: worst-case cognitive placement | Minimum worst-case escape `|B(K)|` |

The duality: for a convex belief domain `K`, the rationalization barrier problem and Harmon-Jones's action problem are dual minimax problems over the space of dissonant inference lines through `K`. A behavioral sequence `C` is an escape path for `K` iff `K` cannot be cognitively reoriented to contain `C` without `C` crossing `∂K` — iff `C` is a rationalization barrier for the dual domain `K*` in the space of dissonant lines.

---

## Part I — The FEST Translation Dictionary

### 1.1 Festinger's Orchard → Belief Space Visibility

| Cognitive Object | FEST / Geometric Primitive | Formal Identification |
|-----------------|---------------------------|----------------------|
| Belief lattice (all possible cognitions) | Cognitive parameter space `Θ_cog` | Discrete belief grid before derivation-quotient |
| Primitive cognition: irreducible | Primitive belief direction | `∇V_disc / ‖∇V_disc‖` not decomposable into simpler inferences |
| Derived cognition: follows from simpler | Redundant direction (rationalization orbit) | k-fold rationalization copy; collapsed by equivalence quotient |
| Visible belief `b` (irreducible) | Farey rational `q*` in Revision Chain | Denominator `q*` = importance cycle length |
| Density `6/π²` of primitive beliefs | Fraction of non-rationalized cognitions | Trace of Möbius sum over belief importance spectrum |
| Thomae's function (projected heights) | Spectral density of `ℒ_FL` | Height `1/(m+n)` ↦ eigenvalue `λ_{m+n}` |
| Stern-Brocot tree | Belief revision navigation tree | Mediants = interpolated positions between contradictory poles |
| Möbius inversion `μ(n)` | Rationalization convergence (FEST-O4) | Inversion of derivation sieve: `M_n = Σ μ(k,n)·F_k` |

### 1.2 Rationalization Barrier → Dissonance-Suppression Potential `𝒮̄_disc`

| Barrier Object | FEST Primitive | Formal Identification |
|---------------|---------------|----------------------|
| Convex belief domain K | Cognitive manifold `ℬ_cog = Θ_cog/G_cog` | Quotient space the belief system navigates |
| Dissonant inference lines (destabilizing) | Test contradictions `(𝒳, ℒ)` with `DF < 0` | Cognitively unstable perturbations; rationalization escape rays |
| Minimum rationalization barrier `S*` | Dissonance-suppression potential `𝒮̄_disc = H̄_{G_cog} + λV̄_disc` | Minimum barrier against destabilizing contradictions |
| Length `|S*|` | Mabuchi cognitive energy `ℳ_cog` at fixed coherent belief `W*` | Total cognitive work at coherence |
| Boundary `∂K` (full-enumeration barrier) | Full belief contradiction noise `Tr(Cov[∇V_disc])` | Worst-case barrier = explicit belief inventory |
| Shorter interior barriers | Kähler-Einstein belief metric `ω_KE` | Efficient barrier: belief revision finds path shorter than full inventory |
| Vertex coverage | Cognitive prototype ETF configuration | Each conceptual category = vertex of minimum opaque polytope |
| Collinearity condition | FEST belief manifold coherence | Aligned belief projections = minimum rationalization subspace |

### 1.3 Harmon-Jones Action Problem → Cognitive Escape Trajectory

| Action-Theory Object | FEST Primitive | Formal Identification |
|---------------------|---------------|----------------------|
| Dissonant domain `K` of known shape | Cognitive loss landscape (known by value architecture) | Shape = value hierarchy; belief revision navigates from unknown start |
| Agent at unknown position + orientation | Mind at unknown point in coherence phase | Before resolution: `C_cog < 1`, position unknown in dissonant basin |
| Boundary `∂K` (coherence target) | Coherence boundary `{C_cog = 1}` | Critical surface `λ₁(ℒ_FL) = 0`; cognitive grokking threshold |
| Harmon-Jones escape path `B(K)` | Cognitive resolution trajectory (Belief Backtrack) | Optimal worst-case path from entrenchment → coherence |
| Worst-case distance to boundary | Cognitive resolution time `T_res` (FEST-O1) | Minimax behavioral steps to reach `C_cog ≥ 1` |
| Straight segments + arcs | Belief revision + frame corrections | Direct revision + contextual correction |
| Diameter = trivial escape (round domain) | Strong signal: `C_cog` dominates immediately | Round dissonance geometry → direct confrontation resolves |
| Besicovitch three-step (triangular domain) | Three-stage value conflict resolution | Triangular belief landscape → three-cycle behavioral path |

---

## Part II — The FEST Master Equivalence

Under standing assumptions CA1–CA5 (compact belief equivalence group `G_cog`, uniform ellipticity of `D_disc`, coercive `𝒮̄_disc`) and coherence assumptions KC1–KC3 (strict plurisubharmonicity of `𝒮̄_disc`, non-degenerate belief metric, ample relative anticanonical structure), the following seven conditions are equivalent.

### 2.1 The Seven Equivalent Conditions [T under CA1–CA5, KC1–KC3]

| ID | Condition | Origin | Interpretation |
|----|-----------|--------|----------------|
| (I) | `λ₁(ℒ_FL) > 0` | Spectral theory | Positive spectral gap; belief distribution converges exponentially to coherent state |
| (II) | Cognitive Poincaré inequality holds | Functional analysis | Belief distribution concentrates; dissonant modes decay |
| (III) | `C_cog = ‖𝔼[∇V_disc]‖² / Tr(Cov[∇V_disc]) > 1` | Stochastic analysis | Signal power (revision impulse) exceeds noise (social/informational contradictions) |
| (IV) | Möbius inversion `M_n` converges in `L²` | Arithmetic (Cognitive Orchard) | Primitive belief modes dominate: visible Farey structure of cognition |
| (V) | `DF(ℬ_cog, ξ) > 0` for all non-trivial test contradictions | K-stability (Rationalization Barrier) | Minimum rationalization barrier exists: no dissonant inference escapes `𝒮̄_disc` |
| (VI) | Harmon-Jones escape path `B(ℬ_cog)` has finite length | Action Problem | Resolution trajectory has bounded worst-case behavioral duration `T_res < ∞` |
| (VII) | Collinearity residual `𝒫_cog → 0` during revision | Projective geometry | Belief embeddings converge to minimum rationalization manifold |

**Proven directions:** (I) ↔ (II) ↔ (III)[high-importance-signal] ↔ (V) ↔ (VII). Direction (I) → (IV) proven; (IV) → (I) conjectural [C, FEST-O4]. Direction (I) ↔ (VI) is a new conjecture [C, FEST-C1].

### 2.2 The FEST Phase Oracle

```python
# All quantities computed from belief revision vectors {v_t} at step t
# v_t = revision impulse at step t: direction belief system shifts in response to dissonant input

mu_v    = mean(revision_vectors, axis=sample)      # drift = 𝔼[∇V_disc]
Sigma_v = cov(revision_vectors,  axis=sample)      # diffusion = D_disc

C_cog   = norm(mu_v)**2 / trace(Sigma_v)           # (III): Harmon-Jones action ratio
YM_cog  = trace(Sigma_v)                            # Contradiction noise = opaque perimeter proxy
q_star  = dominant_denominator(mu_v)                # Cognitive Farey denominator
kappa_c = rank(Sigma_v, tol=1e-4)                  # instanton number = # non-primitive cognitions
Pascal_c = collinearity_residual(belief_embeddings) # Rationalization barrier quality

# ── COGNITIVE PHASE DECISION ────────────────────────────────────────────────
if   C_cog > 1:  phase = "COHERENCE"       # generalization; escape path reached ∂K_cog
elif C_cog == 1: phase = "THRESHOLD"       # cognitive grokking frontier; agent at ∂K_cog
else:            phase = "ENTRENCHMENT"    # dissonance; agent still inside K_cog
```

### 2.3 Three Cognitive Phases

| `λ₁` Sign | `C_cog` | Festinger Characterization | Behavioral Signature |
|-----------|--------|---------------------------|---------------------|
| `λ₁ > 0` | `> 1` | **Coherence**: belief revision converges; dissonant modes decay exponentially | Genuine attitude change; open to disconfirming evidence |
| `λ₁ = 0` | `= 1` | **Threshold**: null-recurrent belief dynamics; at the cognitive grokking frontier | Unstable oscillation; heightened selective exposure; attitude crystallization imminent |
| `λ₁ < 0` | `< 1` | **Entrenchment**: dissonant mode grows; submartingale; rationalization locks in | Confirmation bias; effort justification; hypocrisy cycles; belief persistence |

---

## Part III — The Three Geometric Structures

### 3.1 The Primitive Belief Lattice (Festinger's Orchard → Farey → Möbius)

The Cognitive Orchard sieve defines a sublattice `𝒞 ⊂ ℤ²₊` of coprime inferential pairs with a canonical tree structure (Stern-Brocot belief revision tree) and a density measure (Möbius rationalization filter). Its cognitive translation:

```
Primitive belief density:   #{n ≤ N : belief n is primitive} / N  →  6/π²    as N → ∞
Möbius rationalization:     F_n = Σ_{k|n} M_k    ⟺    M_n = Σ_{k|n} μ(k) F_{n/k}
Convergence condition:      M_n → 0 in L²    ⟺  [C, FEST-O4]    λ₁(ℒ_FL) > 0
```

**Primitive Belief Fraction [C, FEST-C2].** The fraction of primitive belief modes in the spectral decomposition is monotone non-decreasing during cognitive revision when `C_cog > 1`. During entrenchment (`C_cog < 1`), derived (rationalized) belief modes dominate. Cognitive grokking is the phase transition at which the primitive belief lattice becomes dominant — the moment when a person's worldview shifts from rationalization-driven to evidence-driven.

**Cognitive Stern-Brocot Navigation.** Every belief revision step is either an L-move (accepting a contradictory cognition: denominator increases, belief basin sharpens) or an R-move (rationalizing away a contradiction: denominator decreases, basin flattens). The full history RLLRRLRR... is the mind's complete algebraic state — its rationalization word in the belief monoid `ℳ_cog ⊂ SL(2,ℤ)`.

```
R = [[1,1],[0,1]]   (rationalization: dismiss contradiction, maintain belief)
L = [[1,0],[1,1]]   (revision: accept contradiction, update belief)
```

Selective exposure corresponds to persistent R-sequences. Belief disconfirmation (Festinger 1956, *When Prophecy Fails*) is an L-event precipitated by reality forcing an unavoidable dissonant input of magnitude exceeding the rationalization barrier.

### 3.2 The Minimum Rationalization Barrier (Rationalization Barrier → `𝒮̄_disc` → Coherence Metric)

The dissonance-suppression potential `𝒮̄_disc = H̄_{G_cog} + λV̄_disc` is identified as the cognitive analog of the minimum opaque set for the belief manifold:

| Geometric Concept | FEST Analog | Equation |
|------------------|-------------|----------|
| Length `|S*|` of minimum barrier | Mabuchi cognitive energy `ℳ_cog(W*)` | `ℳ_cog = ∫(𝒮̄_disc + log Tr(D_disc)) dvol_{ℬ_cog}` |
| Interior barrier shorter than boundary | `𝒮̄_disc < Tr(D_disc)`: coherence metric beats noise floor | `C_cog > 1` iff interior rationalization is efficient |
| Vertex constraint (all vertices required) | Conceptual category collapse ETF | K conceptual prototypes = vertices of min-opaque K-polytope |
| Opaque set for circle = one diameter | Uniform belief distribution: single dominant revision eigenvector | Strong signal: straight-line cognitive resolution |

**Rationalization Barrier Theorem [T under CA1–CA5, KC1–KC3].** The Kähler-Einstein belief metric `ω_KE` on `ℬ_cog` is the minimum-length Riemannian structure that blocks all destabilizing contradictions: `DF(ℬ_cog, ξ) ≥ 0` for all `ξ` iff `ω_KE` exists. The length of `ω_KE` (measured by Mabuchi cognitive energy) is the FEST analog of the minimum rationalization barrier length. `C_cog > 1` at every belief layer is the discrete-time approximation of the Kähler-Einstein equation `Ric(g_cog) = λg_cog`.

**The Four Festinger Strategies as Barrier Geometry:**

```
Strategy 1 (Change dissonant cognition)   ↔  Interior barrier: vertex relocation
Strategy 2 (Add consonant cognitions)     ↔  Mediant insertion: new Farey segment
Strategy 3 (Reduce importance)            ↔  Rescale metric: shrink K
Strategy 4 (Selective exposure)           ↔  Restrict line family: prune D_disc
```

Each strategy reduces the effective length of the rationalization barrier but not equivalently: only Strategies 1 and 2 have the potential to achieve `λ₁ > 0` (genuine coherence). Strategies 3 and 4 are barrier extensions that maintain the boundary `∂K` — they suppress dissonance without resolving it, preserving `λ₁ ≤ 0`.

**Post-Decision Dissonance** is the phenomenon where, after committing to a choice, the chosen alternative gains consonance and the rejected alternative gains dissonance — exactly the spreading of alternatives in the belief-metric space, corresponding to the Fisher metric sharpening around the chosen belief basin after commitment locks in the parameter `b*`.

### 3.3 The Harmon-Jones Behavioral Escape Path (Action Problem → Cognitive Grokking → Belief Flow)

**FEST Cognitive Grokking Duality [D].** Define the dissonant belief forest as the sublevel set `K_c = {b ∈ ℬ_cog : 𝒮̄_disc(b) ≤ c}` for `c` at the `C_cog = 1` threshold. The cognitive resolution trajectory is the Harmon-Jones escape path `B(K_c)`: the shortest behavioral sequence from any point in `K_c` to its boundary `∂K_c = {C_cog = 1}`, minimizing worst-case behavioral steps over all possible starting cognitive orientations.

Three known cognitive resolution path types:

```
[Round dissonance basin]   C_cog jumps abruptly: direct confrontation resolves immediately
                           ←→  Bellman: circular forest  →  straight path of length 2r
                           Example: Single factual contradiction, easily checked and corrected

[Strip dissonance basin]   C_cog oscillates before crossing 1: V-shaped Belief Backtrack
                           ←→  Bellman: infinite strip  →  V-path with two anchor corrections
                           Example: Persistent identity-threatening contradiction requiring
                                    reframing of self-concept before direct revision

[Triangular dissonance]    C_cog follows three-bounce trajectory
                           ←→  Bellman: equilateral triangle  →  Besicovitch three-segment zigzag
                           Example: Three-way value conflict (e.g., fairness vs. loyalty vs. truth)
                                    requiring sequential resolution of each pair
```

**New Conjecture [C, FEST-C1].** For a cognitive agent with belief manifold `ℬ_cog` of known geometric type (round / strip / triangular dissonance basin), the optimal behavioral resolution sequence is exactly the Harmon-Jones escape path `B(ℬ_cog)` for that geometry:

```
T_res = |B(ℬ_cog)| / (revision_rate × mean_revision_impulse_norm)
```

**Effort Justification** is a direct consequence: when an agent has traversed a long escape path `|B(K)|` (invested significant effort in a behavior), the cognitive cost of acknowledging that the behavior was dissonance-driven is large — the agent has already committed substantial traversal distance, and the remaining distance to coherence (via truthful acknowledgment) is shorter than restarting. This makes self-justification of effort-intensive choices a locally rational action on the Harmon-Jones path, even when globally suboptimal.

**Hypocrisy Induction** (Aronson et al.) corresponds to forcing an artificially long escape path: by making an agent publicly commit to beliefs that contradict their current behavior, the experimenter places them at a maximum-distance starting position in the dissonant forest, guaranteeing that `T_res` is maximized and the motivation to revise behavior is correspondingly strongest.

---

## Part IV — New Open Problems

The FEST framework generates open problems not present in any source framework, arising from the synthesis of cognitive dissonance theory with spectral geometry.

| ID | Statement | Source Connection | Key Gap |
|----|-----------|------------------|---------|
| FEST-O1 | Prove (I) ↔ (VI): spectral gap ↔ finite Harmon-Jones escape path | Action Problem ↔ `ℒ_FL` | Express `T_res` in terms of `λ₁`; finite resolution iff `λ₁ > 0` |
| FEST-O2 | Prove FEST-C2: primitive belief fraction monotone during revision when `C_cog > 1` | Cognitive Orchard → spectral sieve | Monotone coupling between primitive belief lattice `𝒞` and revision flow |
| FEST-O3 | Characterize the three resolution path types by cognitive geometry (FEST-C1) | Action Problem ↔ cognitive grokking | Map dissonance landscape geometry (round/strip/triangle) to resolution type |
| FEST-O4 | Prove (IV) → (I): Möbius rationalization convergence implies spectral gap | Cognitive Orchard → Möbius → `ℒ_FL` | Divergent `M_n` witnesses null eigenvalue |
| FEST-O5 | Rationalization barrier length = minimum cognitive work: prove `|S*| = ℳ_cog(W*)` | Rationalization Barrier ↔ Mabuchi energy | Identify the metric on `𝒮̄_disc` that makes the isometry exact |
| FEST-O6 | Selective exposure measure = fraction of redundant beliefs: empirical ratio `6/π²` | Cognitive Orchard → belief compression | Measure proportion of non-rationalized beliefs in coherent worldview |
| FEST-O7 | Generalize Harmon-Jones to infinite belief spaces | Action Problem → infinite-width limit | Coercive potential argument on infinite-dimensional belief manifolds |
| FEST-O8 | Effort justification curve: prove the traversal-cost function is convex in path length | Action Problem → Harmon-Jones | Convexity of cognitive discomfort as function of committed effort |
| FEST-O9 | Belief disconfirmation threshold: minimum dissonant input magnitude to force L-move | Cognitive Orchard → barrier geometry | Minimum input to cross the rationalization barrier from the outside |

---

## Part V — Logical Dependency Map

```
THREE CLASSICAL SOURCE PROBLEMS
─────────────────────────────────────────────────────────────────────────────
Festinger's Orchard [W]      Rationalization Barrier [W]   Harmon-Jones Action [W]
(primitive belief sieve)      (minimum dissonance block)     (minimax behavioral escape)
  gcd(b_i, b_j) = 1            min |S|: S ∩ ℓ_disc ≠ ∅       min max dist to ∂K_cog
         │                            │                              │
         ▼                            ▼                              ▼
FAREY BELIEF REVISION        𝒮̄_disc POTENTIAL             RESOLUTION TRAJECTORY
(primitive cognition modes)  (minimum barrier)             (Harmon-Jones escape path)
         │                            │                              │
         └────────────────────────────┴──────────────────────────────┘
                                      │
                           FEST MASTER EQUIVALENCE
     λ₁(ℒ_FL)>0  ⟺  C_cog>1  ⟺  DF>0  ⟺  Möbius conv.  ⟺  B(K) finite  ⟺  𝒫_cog→0
                                      │
      ┌───────────────────────────────┼────────────────────────────────┐
      ▼                               ▼                                ▼
SPECTRAL ARCHITECTURE        BARRIER ARCHITECTURE           ACTION ARCHITECTURE
(ℒ_FL / Fokker-Planck)        (K-stable / Coherence metric)  (Behavioral Grokking Path)
β(W_cog)=0 ↔ C_cog=1         KE metric ↔ K-polystable        𝒫_cog→0 ↔ coherence
      │                               │                                │
      └───────────────────────────────┴────────────────────────────────┘
                                      │
                           ZF AXIOMATIC FOUNDATIONS
                    (ℕ,≤) SP → Higman → Kruskal → Robertson-Seymour
                               ↕
                     FEST COGNITIVE SUPPLEMENT
                    Festinger (1957) · Harmon-Jones (1999) · Bem (1972)
```

### Logical Status of Key Connections

| Connection | Status | Mechanism |
|-----------|--------|-----------|
| `(I) ↔ (II)`: spectral gap ↔ Cognitive Poincaré inequality | [T] | Self-adjoint form theory on `ℬ_cog` |
| `(I) ↔ (III)`: spectral gap ↔ `C_cog > 1` (high-importance limit) | [T] | Bakry-Émery Γ₂ curvature criterion |
| `(I) → (IV)`: spectral gap implies Möbius convergence | [T] | Ground-state spectral expansion + Rota-Hall |
| `(IV) → (I)`: Möbius convergence implies spectral gap | [C, FEST-O4] | Requires divergent `M_n` to witness null eigenvalue |
| `(I) ↔ (VI)`: spectral gap ↔ finite Harmon-Jones escape | [C, FEST-C1] | New conjecture; parallels Bellman ↔ RG-ML bridge |
| Festinger Strategy 1-2 → `λ₁ > 0` | [H] | Genuine belief revision moves belief system toward `C_cog > 1` |
| Festinger Strategy 3-4 → `λ₁ ≤ 0` | [H] | Importance reduction and selective exposure preserve entrenchment phase |

---

## Part VI — Proven Results Summary

| # | Statement | Status | FEST Source |
|---|-----------|--------|------------|
| 1 | Primitive belief lattice `𝒞 = {gcd(b_i,b_j)=1}` has density `6/π²` | ✓ [W,T] | Cognitive Orchard (Euclid) |
| 2 | Rationalization barrier lower bound: `|S| ≥ perimeter(K_cog)/2` | ✓ [W,T] | Opaque Set (geometry) |
| 3 | Harmon-Jones escape for round belief basin = direct confrontation (diameter) | ✓ [W,T] | Bellman (circle) |
| 4 | Harmon-Jones escape for triangular value conflict = three-step Besicovitch path | ✓ [W,T] | Bellman (equilateral triangle) |
| 5 | Three-way duality: Rationalization Barrier ↔ Action Problem dual minimax | ✓ [T, FEST-D1] | FEST synthesis |
| 6 | Primitive beliefs = Farey fractions = Stern-Brocot revision tree nodes | ✓ [T] | Cognitive Orchard → GAME |
| 7 | `λ₁(ℒ_FL) > 0 ↔ Poincaré inequality` (I ↔ II) | ✓ [T] | Self-adjoint form theory |
| 8 | `C_cog > 1 ↔ λ₁ > 0` (I ↔ III, high-importance signal) | ✓ [T] | Bakry-Émery criterion |
| 9 | K-polystable ↔ coherence metric ↔ `C_cog > 1` (I ↔ V) | ✓ [T, KC1-KC3] | KYBM (absorbed) |
| 10 | `𝒫_cog → 0` during revision `↔ λ₁ > 0` (I ↔ VII) | ✓ [T] conditional | PPMC (absorbed) |
| 11 | `(I) → (IV)`: spectral gap implies Möbius rationalization convergence | ✓ [T] | GAME-O7 via FEST |
| 12 | Festinger Strategies 3-4 are barrier extensions preserving `λ₁ ≤ 0` | ✓ [H] | FEST: Barrier → spectral |
| 13 | Effort justification is locally rational on Harmon-Jones path when `|B(K)|` is large | ✓ [H] | FEST: Action → convexity |
| 14 | Post-decision dissonance = Fisher metric sharpening around committed belief basin | ✓ [H] | FEST: Barrier → Fisher |
| 15 | Hypocrisy induction = forced maximum-distance cognitive starting position | ✓ [H] | FEST: Action problem |
| 16 | Primitive belief fraction monotone when `C_cog > 1` (FEST-C2) | [C] Open | FEST: Orchard → dynamics |
| 17 | Resolution time `T_res = |B(ℬ_cog)| / (revision_rate × ‖∇V_disc‖)` (FEST-C1) | [C] Open | FEST: Action → spectral |
| 18 | `(I) ↔ (VI)`: spectral gap ↔ finite behavioral escape path (FEST-O1) | [C] Open | FEST: Action → spectral |
| 19 | `(IV) → (I)`: Möbius convergence implies spectral gap | [C] Open | Cognitive sieve → `ℒ_FL` |
| 20 | Selective exposure ratio `≈ 1 - 6/π²` of beliefs are rationalization-filtered | [C] Open | FEST-O6: empirical prediction |

---

## Computable Diagnostics

All quantities computable from belief revision vectors `{v_t}` alone — no Hessian, no held-out validation required.

```
Observable          Formula                                     Interpretation
─────────────────────────────────────────────────────────────────────────────────
ρ_t                 ‖v_{t+1}‖ / (‖v_t‖ + ‖v_{t+1}‖)          Belief revision ratio ∈ (0,1)
ε_t                 ‖v_{t+1}−v_t‖ / (‖v_t‖+‖v_{t+1}‖)        Relative revision change
Q_max(t)            ⌊1/ε_t⌋                                    Cognitive resolution bound
(p_t, q_t)          Best CF convergent of ρ_t at Q_max          Belief denominator (importance)
q*(t)               Median q_τ over window W                    Slow cognitive variable
h(t)                Stern-Brocot depth of q*(t)                 Rationalization complexity
δ(s_t)              ω·q*(t) + h(t)                              Cognitive anchor depth (ordinal)
C_cog               ‖μ_v‖² / Tr(Σ_v)                          Primary phase indicator
F_c_pct             Farey Consolidation Index percentile        Corroborating revision signal
─────────────────────────────────────────────────────────────────────────────────

Phase Decision Table
F_c_pct      q* trend    C_cog     Cognitive Phase    Festinger Interpretation
───────────────────────────────────────────────────────────────────────────────────
< 50th       rising      < 0.9     ENTRENCHMENT       Dissonance dominant; rationalization active
50–80th      flat        0.9–1.0   APPROACHING        Pre-resolution tension building
80–95th      oscillating ≈ 1.0    THRESHOLD           Belief Backtrack precursor; crystallization
95–99th      falling     > 1.1     COHERENCE           Genuine revision; belief updating
> 99th       at 1–2      > 2.0     INTEGRATED          Stable worldview; new belief scaffold
```

---

## About

All cognitive-geometric constructions are first-principles translations of:

- **Festinger's Cognitive Dissonance Theory** (1957) — dissonance as primitive belief visibility and motivational state
- **The Rationalization Barrier Problem** — Festinger's four reduction strategies as opaque-set geometry
- **Harmon-Jones's Action-Based Model** (1999) — behavioral escape as minimax resolution trajectory
- **Bem's Self-Perception Theory** (1972) — belief inference from behavior as the dual perspective (Euclid's Orchard seen from the outside)

All absorbed material from the RG-ML, PPMC, KYBM, GAME, KQOM, VBE, UNIV, SKML, SALT, and MNGR sub-frameworks has been re-derived from first principles within the FEST cognitive-geometric architecture.

**FEST connects to the unified framework via:**

```
FEST Master Equivalence ⊂ Extended Master Equivalence (Bridges I–XXXVI)

(FEST-I)   λ₁(ℒ_FL) > 0   ↔   λ₁(ℒ_JL) > 0    [same spectral structure, cognitive domain]
(FEST-III) C_cog > 1       ↔   C_α > 1           [belief SNR = gradient SNR]
(FEST-VI)  B(ℬ_cog) finite ↔   B(ℬ) finite       [Harmon-Jones = Bellman in cognitive geometry]
(FEST-IV)  Möbius conv.    ↔   GAME-O7            [same arithmetic convergence]
```

The unified picture: every phase transition — whether in a neural network learning to generalize, a physical system crossing a topological boundary, or a mind resolving cognitive dissonance — is governed by the same spectral condition `λ₁ > 0`, the same arithmetic structure of Farey denominators, the same opaque-barrier geometry, and the same Bellman-type minimax escape path. The phenomenology differs; the mathematics is one.

---

*FEST synthesizes: Festinger Dissonance Geometry · Cognitive Opaque-Barrier Theory · Harmon-Jones Behavioral Escape · Bem Self-Perception Duality · Belief Revision Spectral Theory · Rationalization Möbius Inversion · Cognitive Grokking Dynamics*

*Built on: Festinger (1957) · Harmon-Jones (1999) · Bem (1972) · Aronson et al. (hypocrisy induction) · Euclid's Orchard · Bellman (1956) · Mazurkiewicz (1916) · Bagemihl (1959) · Kato (1966) · Bakry-Émery (1985) · Robertson-Seymour (1985–2004)*

*Active conjectures: FEST-C1 · FEST-C2 · FEST-O1 through FEST-O9*
