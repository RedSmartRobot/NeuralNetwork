# Demo: How Neural Networks Learn
## A Demonstration for Law Students

---

### What Is a Neural Network?

A neural network is a mathematical system loosely inspired by the human brain. It consists of
**neurons** — simple computational units — organised in **layers**. The first layer receives
input data; the last layer produces an output (a prediction or classification); intermediate
layers, called **hidden layers**, perform internal transformations. Neurons between adjacent
layers are connected by **weights** — numerical values that determine how strongly one neuron
influences the next.

Learning happens through a process called **training**. The network is shown many examples
with known correct answers. For each example it makes a prediction, compares it to the correct
answer, measures the error, and then adjusts its weights slightly to reduce that error. This
adjustment propagates backwards through the network — hence the term **backpropagation**. After
thousands of repetitions the weights settle into values that allow the network to make accurate
predictions on new, unseen data. The network does not follow explicit rules written by a
programmer; it discovers its own internal patterns entirely from the data it is trained on.

---

### What You See on the Page

The page is divided into two areas. On the **left** is a live visualisation of the neural
network itself. Circles represent neurons, arranged in four vertical columns corresponding to
four layers: the input layer (4 neurons), two hidden layers (6 and 4 neurons), and a single
output neuron on the right. The lines connecting neurons represent weights.

**Before training**, the lines are thin and nearly uniform — the weights are random and the
network knows nothing. **During training**, watch the lines change: they grow thicker as weights
strengthen, and shift in colour — warm golden tones indicate a weight that pushes the risk score
upward, cool blue tones indicate a weight that suppresses it. The rightmost neuron gradually
shifts colour from green (low risk) toward red (high risk) as the network learns to discriminate.

On the **right panel** you will find three sections. The **Training Data** table shows the ten
labelled contracts the network learns from — each described by four features: whether it contains
a penalty clause, its duration, the number of parties, and the degree of ambiguous language. Five
contracts are labelled HIGH risk and five LOW risk.

The **Training** section contains a button to start training and a progress bar. Below the bar a
small chart plots the prediction error over time — you should see it fall steeply at first, then
flatten as the network converges. The epoch counter shows how many training iterations have
completed.

Once training is finished, the **Try It** section becomes meaningful. Four sliders let you
describe a hypothetical contract along the same four dimensions. The network instantly produces
a risk score — a percentage — and a verdict. Move the sliders to explore: setting all features
to maximum (long contract, penalty clause, many parties, high ambiguity) should yield a high risk
score; setting them all to minimum should yield a low one. Intermediate combinations reveal the
network's internal logic — and its limitations.

---

### Key Concepts Illustrated

- **Weights and learning**: the visible thickening and recolouring of connections is the actual
  learning process, not a metaphor for it.
- **Black-box nature**: the network produces a number, but there is no simple rule to read off
  *why*. This is the opacity problem central to AI regulation and explainability law.
- **Generalisation**: the network was trained on ten contracts but can score any combination of
  inputs — including ones it has never seen. Whether it generalises correctly depends entirely on
  whether the training data was representative.
- **Sensitivity to training data**: press Reset, then Train again. The error curve and final
  weights will differ slightly each time, because initial weights are random. The same
  architecture, the same data, a different outcome — a challenge for reproducibility in legal
  contexts.
