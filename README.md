Leveraged ESM-2 (Evolutionary Scale Modeling version 2), a cutting-edge protein language model trained via deep transfer learning on millions of diverse protein sequences, to generate rich, contextual embeddings capturing evolutionary, structural, and functional protein information beyond traditional sequence similarity; combined these embeddings with classical amino acid descriptors as input features for supervised machine learning classification of meiosis proteins, followed by applying these feature representations in unsupervised clustering to discover and validate meiosis-related protein groups in protist proteomes.

Investigated the evolutionary role of meiosis in eukaryotes and its hidden presence in protists previously thought asexual; built upon comparative genomics frameworks from Ramesh et al. (2005) and Schurko & Logsdon (2008).

Reviewed and contrasted traditional homology-based approaches (e.g., meiosis detection toolkit using BLAST and PCR) with modern machine learning techniques for detecting divergent meiosis proteins in poorly annotated genomes.

Curated training data comprising six canonical meiosis loci (e.g., SPO11, DMC1, REC8) and non-meiotic housekeeping proteins from NCBI database; used these to build classifiers for proteome-wide prediction in Plasmodium, Trypanosoma, and Entamoeba.

Developed and tuned a supervised learning pipeline using Support Vector Machines (SVM with RBF kernel) and Multi-Layer Perceptrons (MLP), applying approximate Minimum Redundancy Maximum Relevance (mRMR) feature selection to efficiently identify the most informative and non-redundant features from high-dimensional ESM-2 embeddings and amino acid descriptors, improving model interpretability and performance by reducing noise and overfitting; standardized features prior to training to ensure consistent scale and stability.

Trained and evaluated 48 model configurations using 10-fold cross-validation and a 70/30 train-test split, achieving F1 scores ranging from 0.947 to 0.997. However, limitations in generalizability were noted due to the small dataset size, class imbalance, and fundamental genetic structural differences between meiosis and non-meiosis proteins. Future studies should consider including meiotic genes as a distinct third class to improve model robustness.

Applied models to full protist proteomes using amino acid–derived features alongside ESM-2 embeddings from advanced transfer learning techniques, utilizing reduced feature sets of 50 and 100; prediction probabilities were recorded and ranked to identify high-confidence meiosis gene candidates.

Leveraged mRMR-selected reduced-dimension ESM-2 embeddings and amino-acid descriptors of predicted meiosis proteins as input for downstream unsupervised clustering analysis.

Applied HDBSCAN (Hierarchical Density-Based Spatial Clustering of Applications with Noise), an advanced density-based clustering algorithm that identifies clusters of varying shapes and densities while effectively detecting noise and outliers—ideal for complex, high-dimensional biological data—to group high-confidence (>90% probability) predicted meiosis proteins alongside validated meiosis loci, enabling robust discovery of meaningful protein clusters despite inherent data variability.

Conducted sequence similarity searches using BLASTP on clustered proteins to identify known meiosis gene paralogs, orthologs, and homologs by name and functional annotation.

Validated candidate proteins structurally through AlphaFold, a state-of-the-art deep learning-based protein structure prediction tool developed by DeepMind, which accurately models 3D protein conformations from amino acid sequences by leveraging evolutionary data and physical-chemical principles; this structural insight helped support functional hypotheses related to meiosis by revealing conserved folds and potential active sites in predicted meiosis proteins.
Employed UMAP for dimensionality reduction to visualize clusters, facilitating assessment of biological coherence and separation of meiosis-related groups across diverse protist species.

Integrated evidence from clustering results, BLASTP homology, and structural predictions to prioritize novel or borderline candidates for further experimental and computational study.

Combined clustering outputs with machine learning prediction scores to refine candidate lists, effectively reducing false positives and enhancing confidence in meiosis gene discovery.

Proposed a robust pipeline that synergizes machine learning predictions, unsupervised clustering via HDBSCAN, and comprehensive bioinformatics validation—advancing the detection of conserved and divergent meiosis proteins in protists.
