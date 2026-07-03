# Does Direction Matter in Multi-Hop GNNs?

This project investigates whether preserving **edge direction** improves multi-hop
Graph Neural Networks (GNNs) on heterophilous graphs.

I extend **MixHop** with two direction-aware variants:

- **Dir-MixHop** — separately aggregates incoming and outgoing edges at each hop.
- **Hybrid DirMixHop** — combines directional aggregation with standard
  symmetrized propagation to capture complementary structural information.

## Results

The models were evaluated on four directed heterophilous node-classification
benchmarks.

| Model | snap-patents | arxiv-year | chameleon | squirrel |
| --- | ---: | ---: | ---: | ---: |
| MixHop | 45.4 | 50.8 | 39.5 | 39.3 |
| Dir-MixHop | 73.2 | 61.2 | 39.0 | 39.4 |
| **Hybrid DirMixHop** | **73.8** | **63.3** | **40.4** | **40.7** |

Direction-aware aggregation produced substantial gains on the highly asymmetric
citation graphs. The hybrid model achieved the strongest overall results,
suggesting that directional and undirected propagation provide complementary
information.

## Report

📄 **[Read the full project report](https://drive.google.com/file/d/1Xdq7zIjZ7PdN20NsBP2EVpAoK6RaZVRv/view?usp=sharing)**

The report contains the motivation, mathematical formulation, experimental setup,
ablation study, discussion, and limitations.
