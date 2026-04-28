# Beyond Standard LLMs 04 &mdash; Small Recursive Transformers

A companion to Sebastian Raschka's article *[Beyond Standard LLMs](https://magazine.sebastianraschka.com/p/beyond-standard-llms)*. The fourth of five decks unpacking the four post-transformer architecture families.

This deck takes the **small recursive transformer** family: HRM (Hierarchical Reasoning Model, top of the ARC-AGI leaderboard at release) and TRM (Tiny Recursive Model, 7M parameters, $500 to train, beats HRM at a quarter of the size). The mechanism: a small transformer core run recursively, alternating updates of a latent reasoning state and an answer grid, with a learned halting head. The most counter-intuitive single result in the article: replacing self-attention with a pure MLP layer *improved* accuracy on these tasks (74.7% &rarr; 87.4%) &mdash; the recursion, not the mixing operation, is doing the work.

Includes an **interactive recursive trace viewer** that runs a 4&times;4 puzzle through the recursive solver and shows the input, the current refining answer (with cells turning green as they snap to the target), the latent state visualised as a bar histogram that smooths over iterations, and the halt probability climbing toward the threshold.

**Live site:** https://brendanjameslynskey.github.io/Raschka_Beyond_LLMs_04_Small_Recursive_Transformers/

## Companion deck series

| # | Deck | Architecture family |
|---|------|---------------------|
| 01 | [Linear-Attention Hybrids](https://brendanjameslynskey.github.io/Raschka_Beyond_LLMs_01_Linear_Attention_Hybrids/) | MiniMax-M1, Qwen3-Next, DeepSeek V3.2, Kimi Linear &middot; gated DeltaNet &middot; KV-cache calculator |
| 02 | [Text Diffusion Models](https://brendanjameslynskey.github.io/Raschka_Beyond_LLMs_02_Text_Diffusion/) | LLaDA, Gemini Diffusion &middot; iterative denoising &middot; diffusion-vs-AR visualiser |
| 03 | [Code World Models](https://brendanjameslynskey.github.io/Raschka_Beyond_LLMs_03_Code_World_Models/) | CWM 32B &middot; world-modelling mid-training &middot; rollout stepper |
| 04 | [Small Recursive Transformers](https://brendanjameslynskey.github.io/Raschka_Beyond_LLMs_04_Small_Recursive_Transformers/) | HRM, TRM &middot; iterative self-loops &middot; recursive trace viewer |
| 05 | [When to Reach for Non-Transformer](https://brendanjameslynskey.github.io/Raschka_Beyond_LLMs_05_Decision_Tree/) | Synthesis &middot; decision-tree walker |

Part of the [Modern Architectures sub-hub](https://github.com/BrendanJamesLynskey/LLM_Hub_Modern_Architectures).
