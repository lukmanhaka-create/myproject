# Triad Consciousness Model
### A Computational Phenomenology Framework

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/[USERNAME]/triad-consciousness/blob/main/Triad_Consciousness_Model.ipynb)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Paper](https://img.shields.io/badge/Paper-PDF-blue.svg)](paper/triad_consciousness_paper.pdf)

> *"Bridging phenomenological depth with mathematical rigor"*

---

## 📋 Overview

The **Triad Consciousness Model** is a novel computational framework that integrates phenomenological description with mathematical formalism to explain:

- ✨ **Subjective time distortion** (why time flies in flow, drags in suffering)
- 🧠 **Dissociative states** (from normal awareness to "actual death")
- 🔄 **State transitions** (how consciousness moves between configurations)
- 🏥 **Clinical applications** (diagnosis and treatment implications)

### Three Layers of Consciousness

```
AE (Existential-I)  = 1           [Constant ground]
AA (Actual-I)       = 1 + a·i     [Hybrid awareness, a ∈ {0,1}]
AK (Contextual-I)   = b·i         [Context valence, b ∈ {-1,0,1}]

Total State: S = 2 + (a+b)·i
```

### Six Fundamental States

| State | Coordinates | Name | Phenomenology |
|-------|-------------|------|---------------|
| (0,-1) | 1 - i | Alienated NC | Disconnected, unaware |
| (0,0) | 1 | Autopilot | Mechanical routine |
| (0,1) | 1 + i | Absorbed NC | Lost in distraction |
| (1,-1) | 2 | Suffering | Conscious misery |
| (1,0) | 2 + i | Normal | Baseline waking |
| **(1,1)** | **2 + 2i** | **Flow** | **Optimal engagement** |

---

## 🚀 Quick Start

### Option 1: Google Colab (Recommended - No Installation)

1. Click the "Open in Colab" badge above
2. Run all cells: `Runtime` → `Run all`
3. Interact with generated widgets and visualizations
4. Download figures for your own use

### Option 2: Local Jupyter

```bash
# Clone repository
git clone https://github.com/[USERNAME]/triad-consciousness.git
cd triad-consciousness

# Install dependencies
pip install -r requirements.txt

# Launch notebook
jupyter notebook Triad_Consciousness_Model.ipynb
```

### Option 3: Quick Test

```python
from triad_model import TriadConsciousnessModel

# Initialize
model = TriadConsciousnessModel()

# Get flow state info
info = model.state_info(a=1, b=1)
print(f"Flow State: S = {info['S']}, |S| = {info['magnitude']:.2f}")

# Output: Flow State: S = (2+2j), |S| = 2.83
```

---

## 📊 Key Features

### 1. **Complete Model Implementation**
- Core mathematical functions (state computation, distance metrics)
- Temporal dynamics (subjective time distortion)
- Internalization dynamics (contextual belief transfer)
- Markov state transitions

### 2. **Interactive Visualizations**
- Complex plane representation with all 6 states
- Temporal distortion plots
- Internalization trajectories
- State transition networks
- Real-time parameter exploration with sliders

### 3. **Clinical Applications**
- 10+ clinical parameter profiles (anxiety, depression, PTSD, addiction, etc.)
- Risk assessment algorithms
- Treatment trajectory simulations
- Recovery pathway predictions

### 4. **Publication-Ready Outputs**
- Auto-generate figures in PDF and PNG (300+ DPI)
- Export data tables in CSV format
- LaTeX-compatible outputs
- One-click export: `export_all_figures_for_paper()`

---

## 📖 Documentation

### Basic Usage

#### Get State Information
```python
# Initialize model
model = TriadConsciousnessModel()

# Check any state
info = model.state_info(a=1, b=-1)  # Suffering state
print(f"Distance: {info['distance']:.2f}")
print(f"Time ratio: {info['time_ratio']:.2f}x")
```

#### Simulate Internalization
```python
# How awareness changes with context exposure
t, trajectory, steady = simulate_internalization(
    a_initial=1.0,      # Start aware
    b_target=0.5,       # Positive context
    I=0.3,              # Low information (vulnerable)
    lam=0.4,            # Moderate susceptibility
    beta=0.1,           # Some reinforcement
    duration=10         # 10 time units
)

# Plot results
plt.plot(t, trajectory)
plt.xlabel('Time')
plt.ylabel('Awareness (a)')
plt.title('Internalization Dynamics')
plt.show()
```

#### Generate Visualizations
```python
# Plot all states in complex plane
plot_complex_plane()

# Show temporal distortion
plot_temporal_dynamics()

# Compare healthy vs vulnerable transitions
P_healthy, states = compute_transition_matrix(lam=0.2, I=0.7, b_context=0)
plot_state_transitions_network(P_healthy, states)
```

#### Clinical Case Simulation
```python
# Simulate 6-month recovery trajectory
t_months, states, infos = simulate_clinical_trajectory(
    initial_state=(0, 1),           # Gaming addiction
    context_sequence=[1, 1, 0.5, 0.5, 0, 0, 0],  # Reducing gaming
    I_trajectory=[0.15, 0.25, 0.35, 0.45, 0.55, 0.65, 0.70],  # Therapy
    lam=0.6,
    beta=0.2,
    duration_months=6
)

# Visualize trajectory (auto-generated)
```

---

## 🔬 Scientific Background

### Theoretical Foundations

The model synthesizes insights from:

- **Husserlian Phenomenology**: Temporal structure (retention-impression-protention)
- **Hierarchical Consciousness Models**: Developmental neuroscience
- **Dissociation Research**: Clinical phenomenology of DPDR
- **Predictive Processing**: Bayesian brain frameworks
- **Complex Systems Theory**: Phase transitions and attractors

### Key Innovations

1. **Discrete-Continuous Synthesis**: Six fundamental states with smooth transitions
2. **Hybrid Awareness Structure**: AA bridges physical and mental realms
3. **Information as Protection**: Formalized role of understanding in mental health
4. **Complex Representation**: Orthogonal real (physical) and imaginary (contextual) axes
5. **Testable Predictions**: Clear empirical validation pathways

### Mathematical Formulation

**Temporal Distortion:**
```
Δt' = Δt × (1 + α · D_self-now)

where D_self-now = (1-a) + α_neg · max(0, -b) · a
```

**Internalization Dynamics:**
```
d(Im(S))/dt = λ · (b_target - a) · (1 - I) · e^(βt)

where:
  I = information/understanding
  λ = susceptibility
  β = reinforcement rate
```

**State Transition Probability:**
```
P_ij = σ(λ · Δ_imag · (1-I))

where σ(x) = 1/(1+e^(-x))
```

---

## 🏥 Clinical Applications

### Parameter Profiles

| Condition | Primary State | I | λ | β | Status |
|-----------|--------------|---|---|---|--------|
| Optimal Flow | (1,1) | 0.9 | 0.1 | 0.0 | ✅ Healthy |
| Normal | (1,0) | 0.7 | 0.2 | 0.0 | ✅ Healthy |
| Anxiety | (1,-1) | 0.4 | 0.5 | 0.15 | ⚠️ Risk |
| Burnout | (1,-1) | 0.3 | 0.5 | 0.2 | 🔴 Clinical |
| Depersonalization | (0,1) | 0.2 | 0.6 | 0.25 | 🔴 Clinical |
| Gaming Addiction | (0,1) | 0.15 | 0.7 | 0.35 | 🔴 Clinical |
| Severe Depression | (1,-1) | 0.2 | 0.5 | 0.2 | 🚨 Critical |
| Psychosis | (0,1) | 0.1 | 0.8 | 0.4 | 🚨 Critical |

### Treatment Implications

**Primary Intervention Targets:**

1. **↑ Increase I (Information)**: Psychoeducation, insight therapy, awareness training
2. **↓ Decrease λ (Susceptibility)**: Boundary work, resilience building
3. **↓ Interrupt β (Reinforcement)**: Break patterns, limit exposure
4. **→ Facilitate State Transitions**: From pathological to healthy states

**Predicted Recovery Pathways:**
- Gaming addiction: (0,1) → (1,1) → (1,0) [6-12 months]
- PTSD: (0,-1) → (1,-1) → (1,0) [12-18 months]
- Depression: (1,-1) → (1,0) → (1,1) [6-12 months with treatment]

---

## 📈 Example Outputs

### Complex Plane Visualization
![Complex Plane](examples/fig1_complex_plane.png)
*Six fundamental states mapped in complex space. Flow state (1,1) at optimal 45° phase angle.*

### Temporal Dynamics
![Temporal](examples/fig2_temporal_dynamics.png)
*Time distortion across states. Suffering (red) shows 2x slowdown, Flow (green) is veridical.*

### Clinical Trajectory
![Trajectory](examples/fig5_clinical_trajectory.png)
*Gaming addiction recovery: State (0,1) → (1,0) over 6 months with increasing I (information).*

---

## 🔧 Advanced Usage

### Custom Parameter Sensitivity Analysis

```python
# Test how parameter changes affect outcomes
I_range = np.linspace(0, 1, 20)
final_states = []

for I in I_range:
    t, traj, _ = simulate_internalization(1.0, 0.5, I, 0.3, 0.1, 10)
    final_states.append(traj[-1])

plt.plot(I_range, final_states)
plt.xlabel('Information (I)')
plt.ylabel('Final Awareness (a)')
plt.title('Protection Effect of Information')
plt.show()
```

### Multi-Context Simulations

```python
# Simulate multiple contexts simultaneously
contexts = {'work': -0.5, 'family': 0.8, 'hobby': 1.0}
weights = {'work': 0.5, 'family': 0.3, 'hobby': 0.2}

# Weighted average context
b_effective = sum(contexts[k] * weights[k] for k in contexts)
```

### Export for Different Purposes

```python
# For paper (PDF, high resolution)
plot_complex_plane()
plt.savefig('figure.pdf', dpi=300, bbox_inches='tight')

# For presentation (PNG, transparent)
plt.savefig('figure.png', dpi=150, transparent=True)

# For web (SVG, scalable)
plt.savefig('figure.svg', format='svg')
```

---

## 📚 Citation

If you use this model in your research, please cite:

```bibtex
@article{hakim2025triad,
  title={A Computational Phenomenology of Consciousness: The Triad Model of Temporal Subjectivity and Contextual Internalization},
  author={Hakim, Lukman},
  journal={[Journal Name]},
  year={2025},
  doi={[DOI when available]}
}
```

**Paper:** [Link to published paper]

**Code:** [![DOI](https://zenodo.org/badge/DOI/[DOI].svg)](https://doi.org/[DOI])

---

## 🤝 Contributing

Contributions are welcome! Areas for improvement:

- **Empirical Validation**: Design and run experiments
- **Neural Correlates**: Map states to brain networks
- **Extended Models**: Multiple contexts, interpersonal dynamics
- **Clinical Tools**: Assessment questionnaires, treatment protocols
- **Educational Materials**: Tutorials, workshops, teaching resources

**How to contribute:**
1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📋 Requirements

```
numpy >= 1.21.0
matplotlib >= 3.4.0
scipy >= 1.7.0
ipywidgets >= 7.6.0
pandas >= 1.3.0
```

All dependencies automatically installed in Google Colab.

For local installation:
```bash
pip install -r requirements.txt
```

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

```
MIT License

Copyright (c) 2025 Lukman Hakim

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

[Full MIT License text]
```

---

## 📞 Contact

**Lukman Hakim**
- 📧 Email: [lukman.hakim@example.com]
- 🌐 Website: [https://your-website.com]
- 🐦 Twitter: [@your_handle]
- 💼 LinkedIn: [your-profile]

**Issues and Questions:**
- Open an issue: [GitHub Issues](https://github.com/[USERNAME]/triad-consciousness/issues)
- Discussions: [GitHub Discussions](https://github.com/[USERNAME]/triad-consciousness/discussions)

---

## 🙏 Acknowledgments

- Phenomenological foundations inspired by Husserl, Sartre, and Merleau-Ponty
- Clinical insights from dissociation research community
- Computational methods from complex systems and predictive processing literature
- Thanks to all contributors and users of this model

---

## 📊 Project Statistics

![GitHub stars](https://img.shields.io/github/stars/[USERNAME]/triad-consciousness?style=social)
![GitHub forks](https://img.shields.io/github/forks/[USERNAME]/triad-consciousness?style=social)
![GitHub watchers](https://img.shields.io/github/watchers/[USERNAME]/triad-consciousness?style=social)

![GitHub last commit](https://img.shields.io/github/last-commit/[USERNAME]/triad-consciousness)
![GitHub issues](https://img.shields.io/github/issues/[USERNAME]/triad-consciousness)
![GitHub pull requests](https://img.shields.io/github/issues-pr/[USERNAME]/triad-consciousness)

---

## 🗺️ Roadmap

### Version 1.0 (Current)
- ✅ Core model implementation
- ✅ Six discrete states
- ✅ Interactive visualizations
- ✅ Clinical parameter profiles
- ✅ Basic simulations

### Version 1.1 (Planned)
- ⏳ Empirical validation studies
- ⏳ Neural network mappings
- ⏳ Extended clinical cases
- ⏳ Parameter estimation tools

### Version 2.0 (Future)
- 🔮 Multi-agent interpersonal dynamics
- 🔮 Real-time monitoring applications
- 🔮 Therapeutic intervention algorithms
- 🔮 AI consciousness implementations

---

## ⚖️ Disclaimer

This model is for **research and educational purposes only**. It is not a substitute for professional medical advice, diagnosis, or treatment. Always seek the advice of qualified health providers with any questions regarding mental health conditions.

---

<div align="center">

**⭐ Star this repository if you find it useful! ⭐**

Made with ❤️ for consciousness research

[Back to top ↑](#triad-consciousness-model)

</div>
