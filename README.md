# Analysis of Character Strength in *Pokémon Unite* Using Data Science Methods

## Introduction

This study aims to establish a ranking of character strength in the multiplayer online battle arena (MOBA) game *Pokémon Unite*. The strength of each character is assessed based on two primary factors: (1) overall win rate and (2) individual win rates against other characters. By incorporating matchup data, this model seeks to uncover nuanced insights that surpass evaluations based solely on personal opinion or raw win rates. This approach adds a new dimension to understanding character strength, potentially benefiting players in optimizing their gameplay strategies.

## Methods

### Data Collection and Processing

Data were collected from the website UniteAPI, which provides comprehensive statistics on character performance. The dataset included 70 different variables related to character interactions and win rates. Prior to analysis, the data were processed to enhance the accuracy of the predictive models.

### Principal Component Analysis (PCA)

To manage the high-dimensional dataset, Principal Component Analysis (PCA) was employed. PCA reduced the 70 variables into one, two, and three principal components while retaining the maximum amount of information possible. This dimensionality reduction facilitated more efficient and interpretable analyses.

[View Characters visualized in 3-D](https://jaylon-nelson-sellers.github.io/Pokemon-Unite-Data-Analysis/)

### Clustering Techniques

Using the one-dimensional PCA data, clustering techniques were applied to group characters into tiers. The optimal number of clusters was determined to be five, as indicated by the elbow method.

#### Elbow Method

The elbow method involves plotting the explained variance against the number of clusters to identify the point where adding another cluster does not significantly improve model fit. The "elbow" point on the graph suggests the optimal number of clusters.

![Elbow Method Graph](/Results/1d_elbow_graph.png)
*Figure 1. Elbow method indicating the optimal number of clusters to be 5.*

### Tier Lists Creation

Based on the clustering results, two tier lists were created:

1. **Five-Tier List**: Groups characters into five tiers reflecting their overall strength.
2. **Fifteen-Tier Detailed List**: Provides a more granular classification of characters.

#### Five-Tier List

![Five-Tier List](/Results/tier_list_5_clusters.png)
*Figure 2. Characters grouped into five tiers based on clustering results.*

#### Fifteen-Tier Detailed List

![Fifteen-Tier List](/Results/tier_list_15_clusters.png)
*Figure 3. Detailed tier list with fifteen clusters for in-depth analysis.*

## Results and Discussion

The clustering accurately grouped characters according to their performance metrics, demonstrating the effectiveness of the methods used. By considering both overall win rates and individual matchups, the model provides a nuanced understanding of character strength.

A noted limitation is the overrepresentation or underrepresentation of certain characters, which the current model does not fully address. Future iterations will incorporate ban rates and pick rates to add further nuance to the analysis.

## Conclusion

This study successfully applied data science techniques to create a nuanced ranking of character strength in *Pokémon Unite*. The integration of matchup data and advanced analytical methods offers players a new perspective on character dynamics within the game. The results will be shared with the community to foster discussion and further refinement of the model.

## Citations
- Gupta, Alind. “Elbow Method for Optimal Value of K in KMeans.” GeeksforGeeks, 6 June 2019, www.geeksforgeeks.org
- elbow-method-for-optimal-value-of-k-in-kmeans/. Accessed 4 Oct. 2024.IBM. 
- “What Is Principal Component Analysis? | IBM.” Www.ibm.com, 8 Dec. 2023, www.ibm.com/topics/principal-component-analysis. Accessed 4 Oct. 2024.
- Jain, Deepak. “Data Preprocessing in Data Mining.” GeeksforGeeks, 12 Mar. 2019, www.geeksforgeeks.org/data-preprocessing-in-data-mining/. Accessed 4 Oct. 2024.
- Kavlakoglu, Eda , and Vanna Winland. “What Is K-Means Clustering? | IBM.” Www.ibm.com, 27 June 2024, www.ibm.com/topics/k-means-clustering. Accessed 4 Oct. 
- scikit-learn. “Sklearn.cluster.KMeans — Scikit-Learn 0.21.3 Documentation.” Scikit-Learn.org, 2019, scikit-learn.org/stable/modules/generated/sklearn.cluster.KMeans.html. Accessed 4 Oct. 2024.---. 
- scikit-learn. “Sklearn.decomposition.PCA — Scikit-Learn 0.20.3 Documentation.” Scikit-Learn.org, 2009, scikit-learn.org/stable/modules/generated/sklearn.decomposition.PCA.html. Accessed 4 Oct. 2024.UniteAPI. “Unite API | Pokémon Unite Meta Tierlist.” Uniteapi.dev, 29 Aug. 2023, uniteapi.dev/meta. Accessed 4 Oct. 2024.