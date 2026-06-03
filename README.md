# 🧠 Neural Network Visualizer

[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/HTML5)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Canvas](https://img.shields.io/badge/Canvas-00C853?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API)
[![ML](https://img.shields.io/badge/Machine%20Learning-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)](https://en.wikipedia.org/wiki/Machine_learning)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](LICENSE)

> An interactive, browser-based neural network visualization tool — watch learning happen in real time.

Neural Network Visualizer lets you **build, train, and explore** neural networks directly in your browser. No libraries, no frameworks — just vanilla HTML, CSS, and JavaScript with the Canvas API. Perfect for students, educators, and anyone curious about how deep learning actually works under the hood.

---

## ✨ Features

| Feature | Description |
|---|---|
| 🏗️ **Architecture Builder** | Drag-and-drop layers to design custom network topologies |
| 📊 **Real-time Training** | Watch weights, biases, and loss update live on the canvas |
| 🎯 **Multiple Datasets** | XOR, Circle, Spiral, Gaussian, and custom point clouds |
| ⚡ **Activation Functions** | Switch between ReLU, Sigmoid, Tanh, and Leaky ReLU |
| 🔄 **Forward & Backprop** | Step through each pass to understand the math |
| 📈 **Loss Curves** | Live charting of training and validation loss |
| 🎨 **Weight Heatmap** | Color-coded connections show weight strength and sign |
| 💾 **Export/Import** | Save and load network configurations as JSON |

---

## 🧬 How Neural Networks Work

A neural network is a function approximator — it learns to map inputs to outputs by adjusting internal parameters (weights and biases).

### Forward Propagation

Data flows **left to right** through the network:

1. Each neuron receives inputs from every neuron in the previous layer
2. Each input is multiplied by its corresponding **weight**
3. A **bias** is added to the weighted sum
4. The result passes through an **activation function** (introducing non-linearity)
5. The output becomes input for the next layer

```
output = activation(Σ(weight × input) + bias)
```

This process repeats layer by layer until the final output is produced.

### Backpropagation

The network **learns** by comparing its output to the expected answer:

1. **Loss** is calculated (how wrong was the prediction?)
2. Using the **chain rule** from calculus, we compute the gradient of the loss with respect to every weight
3. Each weight is updated in the **opposite direction** of its gradient
4. The **learning rate** controls how big each step is

```
new_weight = old_weight - learning_rate × gradient
```

Repeat thousands of times → the network converges on a solution.

---

## ⚡ Activation Functions

| Function | Formula | Use Case |
|---|---|---|
| **Sigmoid** | `1 / (1 + e^-x)` | Binary classification output |
| **Tanh** | `(e^x - e^-x) / (e^x + e^-x)` | Hidden layers, zero-centered |
| **ReLU** | `max(0, x)` | Default for most hidden layers |
| **Leaky ReLU** | `max(0.01x, x)` | Prevents "dying ReLU" problem |

---

## 📊 Datasets

| Dataset | Description | Challenge |
|---|---|---|
| **XOR** | Classic non-linearly separable problem | Tests basic non-linearity |
| **Circle** | Points inside vs outside a circle | Radial decision boundary |
| **Spiral** | Interlocking spiral arms | Complex non-linear boundary |
| **Gaussian** | Two overlapping Gaussian clusters | Probabilistic separation |
| **Custom** | Click to place your own data points | Experiment freely |

---

## 🏗️ Architecture Builder

Design your network visually:

- **Add/Remove Layers** — click `+` between layers or `×` to remove
- **Neuron Count** — adjust neurons per layer with the slider
- **Layer Types** — Input, Hidden, Output (auto-detected)
- **Connections** — fully connected by default; watch them render live

Recommended starting architectures:

| Problem | Architecture |
|---|---|
| XOR | 2 → 4 → 1 |
| Circle | 2 → 8 → 4 → 1 |
| Spiral | 2 → 16 → 16 → 1 |

---

## 🔄 Training Process

1. **Initialize** — weights start as small random values (Xavier initialization)
2. **Forward Pass** — compute predictions for all training examples
3. **Compute Loss** — binary cross-entropy for classification
4. **Backward Pass** — calculate gradients via backpropagation
5. **Update Weights** — apply gradients with the learning rate
6. **Repeat** — each full cycle is one **epoch**

The visualizer shows each step so you can pause, rewind, and inspect values at any point.

---

## 🚀 Installation

No installation required — it runs entirely in the browser.

```bash
# Clone the repository
git clone https://github.com/mayank-dev-15/neural-network-viz.git

# Open in your browser
cd neural-network-viz
open index.html
```

Or simply open `index.html` directly from your file system.

---

## 🎮 Usage

1. **Select a dataset** from the dropdown menu
2. **Build your architecture** using the layer controls
3. **Choose an activation function** for hidden layers
4. **Set hyperparameters** — learning rate, batch size, epochs
5. **Click "Train"** — watch the network learn in real time
6. **Click "Step"** to advance one epoch at a time for closer inspection
7. **Click "Reset"** to randomize weights and start over

**Keyboard Shortcuts:**

| Key | Action |
|---|---|
| `Space` | Play / Pause training |
| `S` | Step forward one epoch |
| `R` | Reset network |
| `D` | Cycle through datasets |
| `A` | Cycle through activation functions |

---

## 📚 Learning Resources

- [Neural Networks and Deep Learning](http://neuralnetworksanddeeplearning.com/) — free online book by Michael Nielsen
- [3Blue1Brown: Neural Networks](https://www.youtube.com/playlist?list=PLZHQObOWTQDNU6R1_67000Dx_ZCJB-3pi) — visual intuition series
- [Stanford CS231n](http://cs231n.stanford.edu/) — convolutional neural networks course
- [TensorFlow Playground](https://playground.tensorflow.org/) — similar interactive tool
- [Keras Documentation](https://keras.io/) — practical deep learning library

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

<p align="center">
  Built with ❤️ by <a href="https://github.com/mayank-dev-15">mayank-dev-15</a> — exploring AI one neuron at a time.
</p>
