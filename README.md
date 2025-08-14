# Project Title : Unsupervised Speech Emotion Recognition (SER) using a Lexical-Paralinguistics Hybrid Approach

This project explores an unsueprvised framework for Sppech Emotion Recogniton (SER) by combining lexcial features (what is being said). We leverage Small Languague Models (SLMs) to generate lexical features and a dedicated audion analysis tool for Paralinguistics (how something is being said) features to improve the clustering of speech emotions without relying on lableled data. 


### Introduction 

Traditional SER systems often rely on supervised learning with expensive, labeled datasets, which can be a significant barrier to entry, especially for different languages or domains. This project addresses this limitation by proposing an

Our core hypothesis is that fusing both lexical and paralinguistic features can lead to more semantically coherent clusters and better emotion recognition. We demonstrate that incorporating SLMs into this unsupervised approach can significantly improve clustering performance, circumventing the need for labeled data. 

### Methodology 
The project pipeline involves several key steps:

- Feature Extraction: Paralinguistics Features and Lexcical Features. 
- Feature Fusion: The paralinguistic and lexical features are concatenated to create a combined feature set, which allows the model to jointly consider both what is said and how it is said.
- Dimensionality Reduction: We used UMAP (Uniform Manifold Approximation and Projection) to reduce the dimensionality of the combined features. This step aids in visualization and improves the clustering process.
- Clustering: The final step involves using the K-Means clustering algorithm to group the data points. While we also experimented with HDBSCAN, K-Means provided more interpretable and balanced cluster assignments despite having slightly lower quantitative metrics.





### Results and Evaluation 
We evaluated our model using three key metrics : 

    1. Silhouette  Score 
    2. Davies-Bouldin Index (DBI)
    3. Calinski-Harabasz Index (CHI)

Our Hybrid Approach, which incorporated lexcial features via an SLM, showed a significant improvement over the baseline model (paralinguistic featues only). 

### Limitations and Future Works: 
This project has several limitations that can be addressed in future work:
- Hyperparameter Tuning: We were unable to perform extensive hyperparameter tuning due to time and resource constraints. Further optimization could lead to better results.
- Dataset Variety: The dataset was small and primarily limited to English speech. Future work should include a larger, more diverse dataset with various languages to test the model's adaptability.
- SLM Exploration: We only evaluated three SLMs (BERT, DistilBERT, and RoBERTa). Exploring a wider range of models could lead to more efficient and cost-effective solutions.
