# Vortical Progression: The Dynamic Baseline of History

**Vortical Progression** is the mechanism by which human civilization aggregates the tools, ideologies, and **Rules** of one era into the foundation of the next.

## The Axes
The vortex moves through three dimensions:

- **x — Time:** The only constant axis. Always forward, never reversible. Measured in years; negative values are BC, positive are AD.
- **y — Capability:** What humans can do. Scaled 0–100: 0 is suppressed, 100 is the highest available. The accumulated tools, technologies, and knowledge at any given moment.
- **z — Governance:** What rules, norms, and structures govern the use of that capability — laws, cultural agreements, enforcement mechanisms, access controls. Scaled 0–100: 0 is low or absent, 100 is dominant and calcified.

The relationship between y and z at any point in time determines which arc of the cycle civilization is in. See: **[Cycles Over Time](./cycles-over-time.md)**.

## The Mechanism
Civilization does not move in a straight line or a closed loop; it moves in a vortex. Each historical cycle—though often driven by those seeking mastery or conquest—results in a shifting baseline. As the "Rules" and technologies of previous winners accumulate, they form the "floor" for the next frontier.

## The Equation

Two components: the arc you're in, and the floor you're standing on.

**Arc State** — at any point in time x, civilization occupies a position in (y, z) space:

```
Arc(x) = f( y(x), z(x), ẏ(x), ż(x) )
```

The arc is determined by the gap between y and z and the direction each is moving:

| Condition | Arc |
|---|---|
| y >> z | The Frontier |
| y > z, ż > 0 (winner-controlled) | The Enclosure |
| z ≥ y, stable | The Settlement |
| z >> y, ż ≈ 0, ẏ ≤ 0 | The Grip |
| ż < 0, ẏ > 0 | The Fracture |
| Post-Fracture, VP rises | → New Frontier |
| Post-Fracture, VP falls | → The Collapse |

**Accumulated Floor** — civilization does not reset between cycles:

```
VP(n) = F₀ + Σᵢ₌₁ⁿ εᵢ · Bᵢ
```

- **VP(n)** = the baseline after n cycles — the floor from which cycle n+1 begins
- **F₀** = the inherited floor at the start of the first observed cycle
- **εᵢ ∈ {+1, −1}** = cycle direction: +1 if the Fracture resolved constructively, −1 if it collapsed
- **Bᵢ** = the Books encoded during cycle i — the aggregate of Rules, tools, and ideologies the winners locked in

A run of constructive cycles compounds upward. A destructive Fracture subtracts — and if the Collapse is severe enough, it can set the next cycle back centuries. εᵢ · Bᵢ is Rule Books plus History Books in compact form.

**Moore's Law as Accelerant** — in technology-driven Frontiers, Capability compounds exponentially:

```
y(x) ≈ y₀ · 2^(x / τ)     where τ ≈ 2 years
```

This means ẏ(x) >> ż(x) structurally — Governance can never close the gap in real time. Each doubling produces a new unregulated surface before rules form for the last one. The Frontier phase shortens; the Enclosure arrives faster.

**The Visualization** — plotted parametrically in 3D (x = years, y = Capability 0–100, z = Governance 0–100):
```
x(t) = t / 1000

y(t) = (36 + 29/(1+e^{-t/2000}) + (1 - 1/(2+2e^{-t/2000}))*(20sin(t/1000) + 10sin(t/300) + 5sin(t/80))) / 10

z(t) = (36 + 29/(1+e^{-t/2000}) + (1 - 1/(2+2e^{-t/2000}))*(20cos(t/1000) + 10cos(t/300) + 5cos(t/80))) / 10
```
(t,
  36 + 29/(1+e^{-t/2000}) + (1 - 1/(2+2e^{-t/2000}))*(20sin(t/1000) + 10sin(t/300) + 5sin(t/80)),
  36 + 29/(1+e^{-t/2000}) + (1 - 1/(2+2e^{-t/2000}))*(20cos(t/1000) + 10cos(t/300) + 5cos(t/80)))
```

t from −10,000 to 2026. The sigmoid floor rises as civilization accumulates — slow at the start, steepening through the Common Era, approaching its ceiling in the present. Three overlapping cycle frequencies represent civilizational (~6,280-year), empire-scale (~1,885-year), and regime-scale (~503-year) arcs. Governance trails Capability by 90° — it follows, never leads. The path occupies roughly 1–83 of the 0-100 conceptual space — it does not touch the theoretical bounds. 0 and 100 are limits: no society reaches true zero capability (humans are always capable) or true total governance saturation. The axes define the space; the path shows where civilization has actually moved through it.

### Equation Component Reference

| Symbol | Component | Formula | Value/Role |
|--------|-----------|-----------|--------------|
| **t** | Time (years) | — | Input: −10,000 → 2026 |
| **σ(t)** | Sigmoid floor function | `1 / (1 + e^{-t/2000})` | Rises from 0 to 1 over history |
| **F₀** | Inherited baseline floor | — | 36 (starting capability/governance) |
| **29 · σ(t)** | Accumulated lifts | — | Maximum additional floor from constructive cycles |
| **floor(t)** | Total accumulated floor | `36 + 29 · σ(t)` | Current baseline: 36 (−10k BCE) → ~65 (2026 CE) |
| **ε(t)** | Envelope dampener | `1 - σ(t) / 2` | Reduces oscillation as floor rises: 1 → 0.5 |
| **20 sin(t/1000)** | Civilizational cycle | Amplitude 20, period ~6,280 yr | Major epochal shifts |
| **10 sin(t/300)** | Empire cycle | Amplitude 10, period ~1,885 yr | Rise/fall of empires |
| **5 sin(t/80)** | Regime cycle | Amplitude 5, period ~503 yr | Dynasty/paradigm changes |
| **Oscillation Sum** | Combined amplitude | `20 sin(t/1000) + 10 sin(t/300) + 5 sin(t/80)` | All three cycles |
| **x(t)** | Time axis | `t / 1000` | Mapped to 3D space units |
| **y(t)** | Capability axis | `(floor + envelope) / 10` | Scaled to 0–10 visualization space |
| **z(t)** | Governance axis | `(floor + envelope) / 10` | Scaled to 0–10 visualization space |
| **t** | Time (years) | — | Input: −10,000 → 2026 |
| **σ(t)** | Sigmoid floor function | `1 / (1 + e^{-t/2000})` | Rises from 0 to 1 over history |
| **F₀** | Inherited baseline floor | — | 36 (starting capability/governance) |
| **29 · σ(t)** | Accumulated lifts | — | Maximum additional floor from constructive cycles |
| **floor(t)** | Total accumulated floor | `36 + 29 · σ(t)` | Current baseline: 36 (−10k BCE) → ~65 (2026 CE) |
| **ε(t)** | Envelope dampener | `1 - σ(t) / 2` | Reduces oscillation as floor rises: 1 → 0.5 |
| **20 sin(t/1000)** | Civilizational cycle | Amplitude 20, period ~6,280 yr | Major epochal shifts |
| **10 sin(t/300)** | Empire cycle | Amplitude 10, period ~1,885 yr | Rise/fall of empires |
| **5 sin(t/80)** | Regime cycle | Amplitude 5, period ~503 yr | Dynasty/paradigm changes |
| **Oscillation Sum** | Combined amplitude | `20 sin(t/1000) + 10 sin(t/300) + 5 sin(t/80)` | All three cycles |
| **x(t)** | Time axis | `t / 1000` | Mapped to 3D space units |
| **y(t)** | Capability axis | `(floor + envelope) / 10` | Scaled to 0–10 visualization space |
| **z(t)** | Governance axis | `(floor + envelope) / 10` | Scaled to 0–10 visualization space |

**Phase Relationship:** The 90° offset between `sin` (y) and `cos` (z) means Governance always trails Capability — rules form in response to new capabilities, never precede them.

**Vortical Convergence:** The envelope `ε(t) = 1 - σ(t)/2` contracts oscillation amplitude from 100% at −10,000 BCE to 50% in 2026 CE. This represents tightening civilizational swings as accumulated floor stabilizes: Bronze Age collapses moved civilization further than post-WWII recessions.

**On the name:** The path civilization traces through (x, y, z) space is genuinely vortical. The amplitude of oscillation — `(1 - σ/2)` where σ is the sigmoid floor — contracts as the accumulated floor rises. Early history: large oscillations around a low floor. The present: smaller oscillations around a high floor. The loops tighten as time progresses; the radius is not fixed. This is empirically grounded: civilizational swings were larger before the floor stabilized — Bronze Age collapses moved civilization further than post-WWII recessions. The name fits both the path and the mechanism. The accumulation function `VP(n) = F₀ + Σεᵢ · Bᵢ` is what drives it: each cycle's output becomes the floor for the next cycle's input, the rotation is the oscillation between y and z, and the vortical pull is the accumulation itself — constructive cycles compound upward, destructive ones subtract.

---

## Operationalizing the Axes

The axes are defined conceptually above. What follows is how to measure them empirically — the indicator sources, normalization method, data architecture by era, and the constraints that come with the full −10,000 BC to 2026 range.

### Y — Capability

y measures *realized capability as a fraction of era-available potential* — not absolute, not average. A society's y score is its distance to the frontier of its own era. A 70/100 in 1000 CE is genuinely comparable to 70/100 in 2020 CE; the frontier moves, the relative position is the score.

Two sub-dimensions:
- **y₁ — Human capital stock:** health/longevity, cognitive/educational capacity, physical capacity
- **y₂ — Domain activation:** production and access output across the 9 Domains — what capability is actually being deployed

**Suppression signal:** `Δy = y_potential − y_realized`. A large gap at high z-density is diagnostic of The Grip. This is data, not a data limitation.

**Moore's Law modifier:** In technology-driven Frontiers, `ẏ ≈ y₀ · ln(2)/τ` where τ ≈ 2 years. The sigmoid floor does not capture this — it is a separate accelerant on ẏ during digital-era cycles. Each doubling produces a new unregulated surface before rules form for the last one.

**Normalization method:** Distance-to-frontier (Acemoglu-Aghion-Zilibotti, 2006). Define domain-specific frontiers for each era — maximum observed life expectancy, GDP per capita, literacy, energy use per capita among all contemporaneous societies — score each society as a fraction of that frontier, aggregate into composite y. This sidesteps the goalpost problem of fixed-scale indices and enables cross-era comparison.

**Data architecture:**

| Era | Primary Sources |
|---|---|
| −10,000 to −4,000 BC | HYDE 3.3 (population/urbanization), Atlas of Cultural Evolution / D-PLACE (complexity scores), Global History of Health Project (bioarchaeological stature/health) |
| −4,000 BC to 1 CE | Seshat Global History Databank (1,500+ coded variables, 861 polities), GHHP bioarchaeological data |
| 1 CE to 1500 | Maddison Project (GDP per capita benchmarks), Allen Wages (real wages from 1375) |
| 1500–1870 | Clio-Infra (life expectancy, literacy, wages, height — multi-dimensional) |
| 1870–present | AHDI (Augmented HDI, 162 countries, Prados de la Escosura), Barro-Lee educational attainment (146 countries, sex-disaggregated), FRIEND Registry (VO₂ max norms by age/sex), O\*NET/BLS Skills Data |

### Z — Governance

z is not a quality score. High z is not good. The axis carries two dimensions that must not be collapsed:
- **z-density:** Presence, reach, and enforcement of governance — 0 = absent/failed, 100 = total saturation
- **z-character:** Direction — constructive (serves people, enables capability) vs. calcified (preserves winners, suppresses innovation). This is the dimension all existing governance indices miss. Every major dataset treats high scores as normatively positive; this framework does not.

**The calcification gap:** No standalone calcification index exists. z-character must be constructed from V-Dem component decomposition:
- **Calcified signal:** Neopatrimonialism index, clientelism, CSO repression, censorship, exclusion indices, particularistic policy orientation
- **Constructive signal:** Deliberative democracy component, consultation breadth, CSO participation, universalistic policy, judicial accountability, equal access

The harmonic mean of V-Dem Liberal Democracy + Fraser Economic Freedom + Hanson-Sigman State Capacity (Murphy et al., *Journal of Institutional Economics*) is the closest existing proxy for constructive governance — but it is a threshold classification, not a continuous score.

**Three failure modes of z-character** — all produce The Grip through different mechanisms and tend to co-occur:
- Extractive: governance serving winners over people
- Exclusionary: governance serving some people over others (the Crenshaw dimension)
- Ecological: governance serving present over future (environmental governance is a sub-component of z-character, not a separate axis — Earth is the boundary condition governance exists to manage, not a peer variable)

**Data architecture:**

| Era | Primary Sources |
|---|---|
| −10,000 to −4,000 BC | Atlas of Cultural Evolution (political integration scores), archaeological settlement hierarchy — governance is qualitative inference only here |
| −4,000 BC to 1789 | Seshat (administrative hierarchy, legal codes, limits on executive power, centralization, discrimination coding) |
| 1789–present | V-Dem full dataset (531 indicators, decomposed into density and character composites) |
| 1960–2015 | Hanson & Sigman State Capacity Dataset (extractive, coercive, administrative capacity — explicitly separated from regime type) |
| 1950–2020 | Open Access Orders measure — harmonic mean of economic freedom, liberal democracy, state capacity |
| 1998–present | OECD Product Market Regulation indicators (regulatory density in economic domain, OECD countries) |

### Parameter Constraints and Data Splice Points

**Three critical data gaps — not resolvable with existing sources:**
1. Pre-4000 BCE governance: z-density estimates via Seshat exist; z-character does not. Governance before writing is qualitative inference only.
2. No standalone calcification index: z-character must be constructed, not retrieved. The calcified-vs-constructive distinction is the framework's most important measurement problem and its most significant data gap.
3. Intersectional disaggregation before ~1850 is infeasible quantitatively. Individual-level census microdata (IPUMS) begins at 1850; sex disaggregation extends earlier via GHHP and Barro-Lee; compound intersectional analysis (race × gender × class) before 1850 requires qualitative historical reconstruction.

**Temporal splice seams:**
- **Seam 1 (~4000 BCE):** Archaeological proxy to early historical data. Uncertainty widens dramatically before this point and should be explicit, not smoothed.
- **Seam 2 (~1820 CE):** Pre-modern historical estimates to modern statistical series (Maddison/Clio-Infra boundary).

**Intersectionality constraint:** Average y and z scores mask the suppression dynamics the framework is built to expose. A society where 80% of the population scores y=20 is not a y=65 society — it is a society in The Grip with documented internal suppression. The MAIHDA methodology (multilevel analysis of individual heterogeneity and discriminatory accuracy) is the quantitative tool for reading intersectional strata rather than additive adjustments. Average masking is a governance failure signal, not a data limitation.

**Axis independence:** Seshat's principal component analysis finds ~75% of variance in social complexity loads onto a single dimension — suggesting y and z are more tightly correlated historically than the two-axis model assumes. This does not invalidate the framework but requires direct engagement. The phase lag (z follows y, never leads) is one partial resolution; the calcification dynamic (z overtaking y into The Grip) is another. The independence of the axes is not a given — it is a condition that holds during Frontier phases and breaks down during Settlement and Grip.

**Cycle amplitude:** The three overlapping frequencies in the visualization assume equal amplitude. Empirical data will not confirm this. Amplitude weighting is variable and era-calibrated — civilizational swings were larger before the accumulated floor stabilized. Bronze Age collapses moved civilization further than post-WWII recessions.

---

## Neutrality of the Vortex
It is critical to note that a vortex is not inherently upward or downward. It is a dynamic force of aggregation:
*   **Constructive Movement:** Historically, this has resulted in the mitigation of certain environmental traumas and longer human lifespans as better ideologies and healthcare technologies are pulled into the baseline.
*   **Destructive Movement:** The same mechanism can pull destructive ideologies or restrictive rules into the baseline, creating a downward pull if the "winners" or the "fit" prioritize exploitation over betterment.

## The Cumulative Ledger
Whether the progression is constructive or destructive, the "vortex" ensures that the next frontier starts from the aggregate result of the previous ones. The **[Wild West](./wild-west.md)** of tomorrow will always be built on top of the "Rules" that were written today.
