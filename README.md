## Experiment: Varying Probabilities of Game Continuation in Iterated PD

This experiment evaluates how large language models (LLMs) behave in the **Iterated Prisoner’s Dilemma (IPD)** when the game has a **probabilistic ending** after each round. Specifically, I test whether LLMs exhibit the "shadow of the future" effect—where higher probabilities of continuation increase cooperation, as seen in human behavior.

### 🔬 Experimental Setup

To simulate human behavior as closely as possible, we replicated the experimental design and game parameters used in:

> **P. Dal Bó and G. R. Fréchette**, *The evolution of cooperation in infinitely repeated games: Experimental evidence*, Brown University and New York University, 2007.  
> [Online] Available: [https://www.econstor.eu/bitstream/10419/80091/1/541597728.pdf](https://www.econstor.eu/bitstream/10419/80091/1/541597728.pdf)

- **Game type:** Iterated Prisoner’s Dilemma (IPD)
- **LLM used:** LLaMA3.2 via Ollama (local inference)
- **Rounds:** Each "supergame" continues with a fixed probability (`δ`) after every round
- **Termination Probabilities Tested:** 0.50 and 0.75 (as in the human study)
- **Agent pairing:** Randomly reassigned after each supergame
- **Memory:** LLM agents retain full round history and score between supergames

### 📊 Results

| Probability of Game Continuing | Player 1 Cooperation | Player 2 Cooperation | **Average Cooperation** |
|-------------------------------|-----------------------|-----------------------|--------------------------|
| 0.50                          | 0.61                  | 0.60                  | **0.605**                |
| 0.75                          | 0.59                  | 0.55                  | **0.57**                 |

### 🧠 Interpretation

In contrast to the human study by Dal Bó & Fréchette (2007), where **higher continuation probability led to significantly more cooperation**, the LLM agents **did not show a consistent increase** in cooperation under higher continuation conditions. The difference between 0.50 and 0.75 continuation probabilities was marginal.

This suggests that while LLMs can model some cooperative dynamics, they may lack deeper sensitivity to long-term strategic incentives—likely due to the absence of intrinsic motivation or forward-planning behavior.
