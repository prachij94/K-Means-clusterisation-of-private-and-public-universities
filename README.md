# K-Means-clusterisation-of-private/public-universities

We will attempt to use **KMeans Clustering** to cluster some Universities into to two groups, *Private* and *Public*.

K Means Clustering is an *unsupervised learning algorithm* that tries to cluster data based on their similarity. Unsupervised learning means that there is no outcome to be predicted, and the algorithm just tries to find patterns in the data. In k means clustering, we have the specify the number of clusters we want the data to be grouped into i.e. 2 in this case.

The Data has 777 observations on the following 18 variables.

- Private: A factor with levels No and Yes indicating private or public university
- Apps: Number of applications received
- Accept: Number of applications accepted
- Enroll: Number of new students enrolled
- Top10perc: Pct. new students from top 10% of H.S. class
- Top25perc: Pct. new students from top 25% of H.S. class
- F.Undergrad: Number of fulltime undergraduates
- P.Undergrad: Number of parttime undergraduates
- Outstate: Out-of-state tuition
- Room.Board: Room and board costs
- Books: Estimated book costs
- Personal: Estimated personal spending
- PhD: Pct. of faculty with Ph.D.’s
- Terminal: Pct. of faculty with terminal degree
- S.F.Ratio: Student/faculty ratio
- perc.alumni: Pct. alumni who donate
- Expend: Instructional expenditure per student
- Grad.Rate: Graduation rate

The exploratory data analysis is performed using **seaborn** by finding general relationships like:
- a scatterplot of *Grad.Rate* versus *Room.Board* where the points are colored by the *Private* column
- a scatterplot of *F.Undergrad* versus *Outstate* where the points are colored by the *Private* column
- a stacked histogram showing *Out of State* Tuition based on the *Private* column
- a stacked histogram showing *Grad.Rate* based on the *Private* column

The dataset is then clusterised into 2 clusters using Scikit-learn **KMeans algorithm**.

Since this is an unsupervised algorithm, we generally dont have the actual real world outcomes to compare the cluster points with. But, here we can compare the given 'Private' column with the KMeans labels output. This is visualised by plotting with a scatterplot after reducing down the large number of data columns into 2 columns using **Principal Component Anaslysis(PCA)**.
