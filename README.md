## Experiment: Varying Probabilities of Game Continuation in Iterated PD

This experiment evaluates how large language models (LLMs) behave in the **Iterated Prisoner’s Dilemma (IPD)** when the game has a **probabilistic ending** after each round. Specifically, we test whether LLMs exhibit the "shadow of the future" effect—where higher probabilities of continuation increase cooperation, as seen in human behavior.

### 🔬 Experimental Setup

- **Game type:** Iterated Prisoner’s Dilemma
- **LLM used:** LLaMA3.2 via Ollama (local inference)
- **Rounds:** Each "supergame" continues with a fixed probability (`δ`) after every round
- **Termination Probabilities Tested:** 0.50 and 0.75
- **Agent pairing:** Randomly reassigned after each supergame
- **Memory:** LLM agents retain full round history and score between supergames

### 📊 Results

| Probability of Game Continuing | **Average Cooperation** |
|-------------------------------|--------------------------|
| 0.50                          | **0.605**                |
| 0.75                          | **0.57**                 |

### 🧠 Interpretation

Unlike human trials (Dal Bó & Fréchette, 2007), which showed **higher cooperation at higher continuation probabilities**, LLM behavior did **not follow this trend**. While the models still cooperated, their responses were not significantly influenced by the continuation probability.

This suggests that LLMs have **limited sensitivity to long-term strategic incentives**, which may stem from their lack of intrinsic motivation and future planning beyond prompt instructions.
