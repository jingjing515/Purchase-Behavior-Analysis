# Purchase Behavior Analysis for Targeted Customer Segmentation

## Project Overview

This project focuses on segmenting customers based on their purchasing behaviors and preferences, using clustering techniques to create targeted marketing strategies. By analyzing a dataset of 2,240 customers from Kaggle, we identify distinct customer groups to help businesses offer more personalized promotions and products, enhancing customer experience and increasing loyalty.

## Dataset

We used the **Customer Personality Analysis** dataset from Kaggle, which contains detailed information on customers such as demographics, household details, spending categories, online interactions, and responses to marketing campaigns.

- [Kaggle Dataset](https://www.kaggle.com/datasets/imakash3011/customer-personality-analysis)

## Features Engineered

- **Total_Num**: Sum of purchases across different channels (Web, Catalog, Store).
- **Total_Mnt**: Total monetary spend across product categories (Wines, Fruits, Meat, etc.).

## Methods Used

- **Data Preprocessing**: Cleaning missing data, outlier removal, and feature engineering.
- **Dimensionality Reduction**: PCA (Principal Component Analysis) was used to reduce the dataset to three principal components.
- **Clustering Algorithms**:
  - Hierarchical Clustering
  - DBSCAN (Density-Based Spatial Clustering of Applications with Noise)
  - K-means Clustering

## Results

We found that **K-means Clustering** was the most effective for segmenting customers based on their purchasing behavior. The optimal number of clusters was determined using the **Elbow Method**, and the final clusters were evaluated using metrics like **Silhouette Score**, **Calinski-Harabasz Score**, and **Davies-Bouldin Score**.

### Clusters:
1. **Active Shoppers**: High-income, high-frequency shoppers, responsive to marketing.
2. **Cost-Conscious Buyers**: Low-income, low-frequency shoppers, sensitive to discounts.
3. **Family Shoppers**: Middle-income, moderate-frequency shoppers, larger families.

## Key Technologies

- **Languages**: Python (NumPy, Pandas, Scikit-learn)
- **Visualization**: Matplotlib, Seaborn
- **Clustering Techniques**: K-means, DBSCAN, Hierarchical Clustering
- **Dimensionality Reduction**: PCA (Principal Component Analysis)
- **Data Analysis**: Box Plots, Heatmaps, Correlation Matrices

## Usage

To run the code and reproduce the results, clone the repository and ensure you have the required dependencies listed in the `requirements.txt` file. Use the following command to install the dependencies:

```bash
pip install -r requirements.txt
```

Run the notebook `Purchase_Behavior_Analysis.ipynb` to perform data preprocessing, feature engineering, and clustering analysis. The notebook includes the steps for:

1. Cleaning missing data and removing outliers
2. Feature engineering (e.g., creating **Total_Num** and **Total_Mnt**)
3. Applying PCA for dimensionality reduction
4. Implementing Hierarchical Clustering, DBSCAN, and K-means Clustering
5. Evaluating clustering performance using Silhouette Score, Calinski-Harabasz Score, and Davies-Bouldin Score
6. Visualizing the clusters using scatter plots and box plots

### Visualizations

- **Heatmap**: Visualizes correlations among customer features, identifying relationships between purchase categories and other demographic variables (Appendix 2).
- **K-Nearest Neighbors Distances**: Helps optimize parameters for DBSCAN by analyzing distances between nearest data points (Appendix 3).
- **Elbow Method**: Used to determine the optimal number of clusters for K-means, based on changes in inertia values (Appendix 4).

### Evaluation Metrics

The clustering performance was evaluated using three key metrics:

- **Silhouette Score**: Measures how similar data points are within the same cluster. A higher score (closer to +1) indicates well-separated clusters. We obtained a score of **0.443**, showing reasonable separation between clusters.
  
- **Calinski-Harabasz Score**: A higher score indicates better-defined clusters. We achieved a score of **2545.553**, indicating strong clustering performance.

- **Davies-Bouldin Score**: Lower values indicate better separation between clusters. Our score of **0.891** suggests well-defined clusters with minimal overlap.

## Results

After performing the analysis, the customer data was divided into three main clusters:

1. **Active Shoppers**: High-income customers with frequent purchases across multiple categories. Respond well to marketing campaigns and loyalty programs.
2. **Cost-Conscious Buyers**: Lower-income customers who are more price-sensitive. Marketing strategies should focus on discounts and promotions.
3. **Family Shoppers**: Middle-income customers with larger families. Respond moderately to marketing campaigns and tend to shop for family-oriented products.

## Conclusion

The combination of PCA for dimensionality reduction and K-means clustering for segmentation proved effective in identifying distinct customer groups. By leveraging the insights from these customer segments, businesses can tailor their marketing strategies to better address the unique needs and preferences of each group, ultimately enhancing customer engagement and driving sales.

Future improvements could include using additional data sources, such as social media activity or real-time purchasing data, to further refine the segmentation and improve the accuracy of the clusters.

## References

1. [Kaggle Dataset](https://www.kaggle.com/datasets/imakash3011/customer-personality-analysis)
2. Palangad Othayoth S, Muthalagu R. "Customer segmentation using various machine learning techniques," International Journal of Business Intelligence and Data Mining, 2022.
3. Hicham N, Karim S. "Analysis of unsupervised machine learning techniques for efficient customer segmentation," International Journal of Advanced Computer Science and Applications, 2022.
4. Tabianan K, Velu S, Ravi V. "K-means clustering approach for intelligent customer segmentation using customer purchase behavior data," MDPI Sustainability, 2022.



