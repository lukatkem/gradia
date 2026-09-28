# Known limitations

- Scalar autograd only — no shaped tensors, no broadcasting. That is the point:
  nothing is hidden behind a tensor library.
- Full-batch training — mini-batching is a one-loop change away, deliberately
  left as an exercise-shaped gap.
- The demo corpus is tiny; overfitting IS the demonstration that learning works.