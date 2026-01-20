# Customer-Segmentation\

1. Project Overview
This project aims to segment customers into distinct groups based on their purchasing and behavioural patterns. By identifying meaningful customer segments, businesses can design targeted marketing strategies, improve customer retention, and allocate resources more effectively.
Using unsupervised learning techniques, customers were grouped into three actionable segments after evaluating multiple clustering approaches and validation metrics.

2. Business Problem
Many businesses treat all customers as a single group, resulting in inefficient marketing spend and low campaign effectiveness. The objectives of this project are to:
- Identify distinct customer segments
- Understand the key characteristics of each segment
- Provide data-driven recommendations for targeted marketing strategies

3. Dataset
Source: Kaggle
Description: Customer demographic and behavioural dataset
Size: 2,240 rows with 29 features
Includes: Income, education, family structure, spending across product categories, purchase channels, and campaign response

4. Exploratory Data Analysis (EDA)
Exploratory analysis revealed that:
- Most numerical features were right-skewed
- Several spending and purchase frequency variables showed strong positive correlation
- Income alone was not a strong predictor of customer value
- Channel usage and campaign response varied significantly across customers
These findings guided preprocessing decisions and feature selection for clustering.


5. Data Preprocessing
The following preprocessing steps were performed:
- Ordinal encoding for Education
- One-hot encoding for Marital_Status
- Standardisation of non-binary numerical features using StandardScaler
- Missing value handling for binary features using SimpleImputer
- Dimensionality reduction using Principal Component Analysis (PCA) to reduce noise and improve clustering performance

6. Dimensionality Reduction (PCA)
PCA was applied to retain 90% of the total variance, reducing dimensionality while improving computational efficiency and cluster separation

7. Clustering Methodology
Two clustering techniques were evaluated:
- K-Means Clustering
- Hierarchical Agglomerative Clustering (HAC)
The optimal number of clusters was determined using the elbow method and silhouette scores. Both methods consistently indicated that 3 clusters provided the best balance between cluster cohesion and separation.

8. Cluster Analysis and Interpretation
Cluster 0 – Budget-Constrained Families
- Larger households with children and teenagers
- Lower income and lowest overall spending
- Education skewed towards basic or undergraduate levels
- Primarily store-based purchases
- Lowest campaign acceptance and response rates
Business Interpretation:
Low-value and price-sensitive segment with limited short-term ROI.

Cluster 1 – Mainstream Family Shoppers
- Families with older children
- Mid-level income and moderate spending across categories
- Balanced usage across store, web, and catalogue channels
- Moderate deal sensitivity and campaign response
Business Interpretation:
Stable, average-value segment with potential for upselling.

Cluster 2 – Premium Loyalists
- Few or no children
- Highest income and highest spending across most categories
- Less price-sensitive with strong catalogue and store usage
- Highest campaign acceptance and response rates
Business Interpretation:
High-value customers and key contributors to marketing ROI.

9. Business Recomendations
Cluster 0 – Budget-Constrained Families
Recommended Strategy:
- Cost-efficient engagement and selective targeting
- Limit marketing spend due to low response and ROI
- Focus on essential product bundles and price-driven promotions
- Use mass marketing or automated campaigns instead of personalised offers
- avoid premium campaigns for this segment
Expected Outcome:
Reduced marketing costs and improved campaign efficiency.

Cluster 1 – Mainstream Family Shoppers

Recommended Strategy:
- Upselling and cross-selling opportunities
- Promote family-oriented bundles and seasonal offers
- Encourage migration to higher-margin products through personalised recommendations
- Use omnichannel campaigns (store, web, catalogue)
- Test loyalty incentives to increase lifetime value
Expected Outcome:
Gradual increase in average spend and customer lifetime value.

Cluster 2 – Premium Loyalists
Recommended Strategy:
- Retention and exclusivity-focused marketing
- Prioritise this segment for personalised and high-touch campaigns
- Offer exclusive previews, premium memberships, and loyalty rewards
- Avoid excessive discounting as they are less price-sensitive
- Use targeted catalogue and in-store campaigns
Expected Outcome:
Higher retention, stronger brand loyalty, and maximum marketing ROI.
