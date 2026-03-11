We study the impact of data partitioning strategies, feature families, and graph topology
on supervised link prediction over large-scale academic collaboration networks. In contrast
to standard node-partitioned evaluation protocols, we analyze a less studied but widely used
practice in applied graph mining: edge-ordered training, where positive and negative links are
generated from a single evolving graph and then ordered or shuffled before splitting. Using
two real collaboration graphs (UNAM and Stanford), we evaluate multiple supervised pipelines
combining semantic Feature Proximity (FP), Local Structural Proximity (LSP), and Global
Structural Proximity (GSP), trained under both edge-ordered and node-partitioned regimes.
Eight controlled experimental pairs are constructed to isolate the effects of (i) feature type
(semantic vs. topological), (ii) feature cardinality, (iii) graph origin (UNAM vs. Stanford), and
(iv) data partitioning protocol (edges vs. nodes). Models include classical machine-learning
classifiers as well as stacked meta-models trained over base predictors. Performance is assessed
using AUC-ROC, AUC-PR, F1, and Accuracy across repeated runs, and statistical significance
is evaluated using paired Wilcoxon signed-rank tests.
Our results indicate that node-partitioned training often yields higher AUC-ROC and F1
when semantic and mixed FP+LSP+GSP features are used, while edge-ordered training tends
to produce higher scores for purely topological features, a pattern compatible with information
leakage induced by shared neighborhoods. Furthermore, meta-models frequently achieve nearperfect scores under edge-ordered settings but degrade substantially under node-partitioned
splits, suggesting sensitivity to leakage-driven signals rather than purely generalizable structure.
Keywords: link prediction, scientific collaboration networks, graph-based machine learning,
edge-ordered, node-partitioned
