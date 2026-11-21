# Follow-ups on the graph switch chain

Two follow-ups to [OpenAI's Theorem 1.1](https://mathcommunity.github.io/oai-math-revised/papers/Polynomial-Mixing-of-the-Switch-Chain-for-Every-Graphical-Degree-Sequence-September-25-2026/) use the same lazy four-vertex proposal and worst-start total variation threshold of $1/4$.

## All graphical degree sequences

**Result:** The mixing-time upper bound improves from $2n^8$ to $n^6$, without changing the chain or sampler.

**Key step:** The local comparison constant within a fiber drops from $n^2$ to $1/2$ (original Lemma 7.4).

[Read the proof note (PDF)](https://github.com/hys-ops/switch-chain-mixing-followup/blob/cba4fa25e6681cc1d06e21217154cfce3bdc2fac/Switch_Chain_Followup_hys-ops.pdf) · [Lean reproduction kit](https://github.com/hys-ops/switch-chain-mixing-followup/blob/cba4fa25e6681cc1d06e21217154cfce3bdc2fac/Switch_Chain_Lean_Kit_hys-ops.zip) · [Community submission #83](https://github.com/mathcommunity/oai-math-revised/issues/83)

## Unigraphs

**Result:** The worst mixing time over all unigraphic degree sequences is $\Theta(n^4\log n)$. A unigraphic degree sequence has just one isomorphism class of realizations.

**Key step:** Compare the Laplacian $J$ of equal-degree label transpositions with the switch Laplacian $L$: $J\preceq 2L$. The upper bound holds across the class; known hypercube realization graphs give the matching lower order with the original proposal clock.

[Read the 4-page note (PDF)](https://github.com/hys-ops/switch-chain-mixing-followup/blob/6143f8f113c7e441e6571a995bf5ddea8b941abc/Unigraph_Switch_Chain_Public_Review_hys-ops.pdf) · [Lean reproduction kit](https://github.com/hys-ops/switch-chain-mixing-followup/blob/6143f8f113c7e441e6571a995bf5ddea8b941abc/Unigraph_Switch_Chain_Public_Lean_Kit_hys-ops.zip) · [Community submission #85](https://github.com/mathcommunity/oai-math-revised/issues/85)

## Verification and credit

The kits list the Lean-checked statements, proof dependencies and build logs. The unigraph kit includes the matching upper and lower bounds in `UnigraphWorst.worst_theta`. The unigraph note credits prior work, including [Barrus](https://arxiv.org/abs/1503.06073) and [Erdős et al.](https://arxiv.org/abs/1909.02308), and makes no priority claim.

Submitted for review by `hys-ops`. ChatGPT/Codex contributed to the arguments, writing and Lean development. No independent human mathematical review has been recorded. Upstream license notices remain in the kits.
