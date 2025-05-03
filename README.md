# homwork5
### 1. GAN Architecture

**Adversarial Process**:
Generative Adversarial Networks (GANs) consist of two neural networks, a **generator** and a **discriminator**, competing against each other in a zero-sum game.

* **Generator's Goal**: Create data that is indistinguishable from real data. It takes random noise as input and generates fake samples.
* **Discriminator's Goal**: Distinguish between real and generated (fake) data.
* **Improvement Through Competition**: The generator improves by learning to fool the discriminator, while the discriminator becomes better at detecting fake data. This iterative process pushes both networks toward optimal performance.

**Diagram**: A diagram should include arrows showing the data flow: random noise → generator → fake data → discriminator → real/fake label.

---

### 2. Ethics and AI Harm

**Chosen Harm**: Representational Harm
**Example**: A facial recognition system misidentifying individuals from specific demographic groups more often than others.
**Mitigation Strategies**:

1. **Diverse Training Data**: Ensure datasets represent all demographic groups fairly.
2. **Bias Auditing**: Regularly test and refine the system using bias detection tools like Aequitas.

---

### 3. Programming Task (Basic GAN Implementation)

**Overview**:

* **Generator**: Maps random noise to synthetic data. Architecture includes dense and convolutional layers.
* **Discriminator**: Classifies data as real or fake. Uses convolutional layers for feature extraction.
* **Training Loop**: Alternates between updating the generator (using discriminator feedback) and discriminator (using real and fake data).

**Deliverables**:

* Show generated samples at Epoch 0, 50, and 100.
* Plot generator and discriminator loss curves to illustrate learning dynamics.

---

### 4. Programming Task (Data Poisoning Simulation)

**Overview**:

* Train a basic sentiment classifier on a clean dataset.
* Introduce poisoned data by flipping labels for specific entities (e.g., "positive" phrases about "UC Berkeley" marked as "negative").
* Analyze how poisoning affects model accuracy and decision boundaries.

**Deliverables**:

* Accuracy before and after poisoning.
* Confusion matrices showing changes in predictions.

---

### 5. Legal and Ethical Implications of GenAI

**Concerns**:

1. **Memorizing Private Data**: Generative AI models may unintentionally output sensitive information seen during training.
2. **Generating Copyrighted Material**: Models may reproduce copyrighted works, leading to legal and ethical disputes.

**Position**:
Restricting models from training on certain data could mitigate risks but might also limit model capabilities. A balanced approach involving consent and anonymization is ideal.

---

### 6. Bias & Fairness Tools

**Bias Metric**: False Negative Rate Parity

* **What It Measures**: Ensures that false negative rates (misclassifications where a positive class is incorrectly labeled as negative) are consistent across groups.
* **Importance**: Disparities in false negatives can disadvantage specific groups, especially in critical applications like loan approvals or healthcare diagnostics.
* **Failure Scenario**: A model might fail this metric if it disproportionately rejects loan applications for one demographic group, even when they meet the criteria.

**Optional**: Apply Aequitas to analyze a dataset and visualize disparities.
