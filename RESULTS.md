# Measured results

From the deterministic demo run (pure stdlib, no GPU):

- **x² regression** (2→8→1 MLP, 16 samples, 600 epochs): MSE 4.58 → **0.0076**;
  predictions x=−2 → 3.833 (truth 4.0), x=0.5 → 0.245 (truth 0.25)
- **Two-blob classifier** (2→8→8→2, 40 samples, 300 epochs): cross-entropy
  0.612 → 0.0056, accuracy **100%**
- **Gradient checks**: every op matches finite differences to **1e-12**
- Training is bit-identical across runs (topological order by creation serial,
  not memory addresses — the determinism design decision)
