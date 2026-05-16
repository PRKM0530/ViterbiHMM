# ViterbiHMM

Implementation of the Viterbi algorithm using a Hidden Markov Model (HMM) to identify exon-intron boundaries in a DNA sequence.

## Background

Gene prediction is one of the fundamental problems in computational biology. One way to approach this is by modeling the hidden states of a DNA sequence — such as exons, introns, and splice sites — using an HMM. The Viterbi algorithm finds the most probable sequence of hidden states given an observed nucleotide sequence.

## Model

The HMM has 5 hidden states:

- `s` — silent start state
- `E` — Exon
- `5` — 5' splice site
- `I` — Intron
- `e` — silent end state

Each state has defined transition probabilities (how likely it is to move to the next state) and emission probabilities (how likely it is to emit each nucleotide A, C, G, T).

## What the notebook does

1. Manually computes log-probabilities for several hand-picked state paths to build intuition
2. Initializes the Viterbi value matrix and traceback matrix
3. Implements `calculate_prob_for_a_node()` which fills a single cell in the matrix by finding the best previous state
4. Runs nested for loops to fill the entire matrix
5. Traces back through the matrix to recover the most probable state path

## Query sequence

```
CTTCATGTGAAAGCAGACGTAAGTCA
```

## How to run

```bash
jupyter notebook ViterbiHMM.ipynb
```

Run all cells in order. No external data files are needed.

## Dependencies

```bash
pip install numpy
```
