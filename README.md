\# Customer Segmentation with K-Means Clustering



A machine learning project that groups mall customers into distinct segments based on their income and spending patterns. The goal is to help businesses move beyond one-size-fits-all marketing and instead build targeted strategies for each customer type.



\## The Problem



Most businesses treat customers as one big group, but that's rarely effective. A premium customer doesn't respond to the same offers as a budget-conscious one. Identifying natural groupings in customer data lets marketing teams personalize their approach, which usually means higher engagement, better conversion rates, and stronger retention.



This project uses unsupervised machine learning to find those groupings automatically, without any predefined labels.



\## About the Dataset



I used the Mall Customer Segmentation dataset from Kaggle, which contains information about 200 mall customers including:



\- Gender

\- Age

\- Annual income in thousands of dollars

\- Spending score from 1 to 100, where higher means more spending



There is no target variable in this dataset, which is why this is an unsupervised learning problem.



\## Approach



I started by exploring the data through histograms and scatter plots to understand the distribution of age, income, and spending behavior. The income versus spending scatter plot already hinted at distinct customer groups.



Next, I scaled the features using StandardScaler so that income and spending score would be weighted equally during clustering. Without scaling, income values would dominate because they are on a much larger scale.



To find the right number of clusters, I used two techniques:



1\. The Elbow Method, which plots within-cluster sum of squares against different K values to find where the curve bends

2\. The Silhouette Score, which measures how well-separated the clusters are



Both methods pointed to K equals 5 as the optimal number of clusters.



After applying K-Means with K equals 5, I analyzed each cluster by looking at average age, income, and spending behavior. Then I assigned business-friendly names and recommended marketing strategies for each segment.



\## Results



The final model produced 5 well-separated customer segments with a Silhouette Score around 0.55, which indicates good cluster quality.



The five segments I identified were:



\- Premium customers with high income and high spending

\- Cautious affluent customers with high income but low spending

\- Average customers with moderate income and moderate spending

\- Risk takers with low income but high spending

\- Budget-conscious customers with low income and low spending



\## Visualizations



\### Customer Clusters

The main result of the project, showing all five customer segments grouped by income and spending behavior.



!\[Customer Clusters](images/customer\_clusters.png)



\### Finding the Optimal Number of Clusters

The Elbow Method and Silhouette Score both suggest K equals 5 works best.



!\[Elbow Method](images/elbow\_method.png)



\### Cluster Characteristics

Average age, income, and spending score for each cluster.



!\[Cluster Profiles](images/cluster\_profiles.png)



\## What I Learned



Working through this project reinforced a few things for me. First, scaling matters more than I expected, since income on a scale of thousands would have completely dominated spending score on a scale of 1 to 100 if I had skipped it. Second, the elbow method alone is not always conclusive, so combining it with silhouette score gives a more confident decision. Third, the technical work is only half the job. Translating five anonymous clusters into named segments with clear marketing implications is what actually makes the output useful to a business.



\## Business Applications



These segments could be used to:



\- Send personalized email campaigns based on customer type

\- Build targeted promotions for high-value segments

\- Identify which customers need different retention strategies

\- Inform pricing and product positioning decisions

\- Improve overall marketing return on investment



\## Tools and Libraries



\- Python 3.11

\- pandas and NumPy for data manipulation

\- scikit-learn for KMeans, StandardScaler, and Silhouette Score

\- matplotlib and seaborn for visualization

\- Jupyter Notebook for the analysis



\## Running the Project



Clone the repository, install dependencies, and open the notebook:



pip install -r requirements.txt  

jupyter notebook customer\_segmentation.ipynb



\## About Me



I'm Mounika Reddy Madagam, transitioning from 5+ years in Salesforce Marketing Cloud at DIRECTV and Pfizer into Data Science and Machine Learning Engineering. This is my second machine learning project, focused on unsupervised learning techniques.



You can reach me at mrmadagam@gmail.com or connect on LinkedIn at linkedin.com/in/mounika-reddy-b90344230. My other ML projects are on GitHub at github.com/Mounika-Madagam.

