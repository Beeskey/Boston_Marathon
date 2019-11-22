## Target
The goal of this project was to experiment with clustering as a tool for feature engineering.

## Dataset
The data for this project was 2014 Boston marathon participant data including: name, gender, age, country, city, times for various checkpoints (5K, 10K, 15K, etc.), final official time, rank in division, rank in gender division. 

## Tools and Process
To achieve this I use cluster visualizations, silhouette coefficients, and elbow method analysis to determine an ideal number of clusters. From there, I create an KMeans model with the ideal cluster size and add the output as a 'cluster' column to the data set. The final task is understanding what each cluster represents through visualization and statistical analysis, including ratio plots for many features against the clusters.

## Conclusions
I was able to determine ideal cluster size was either 3 or 4, so I performed analyses of both and compared. 
The 3 cluster model story:
- Cluster 1 was the smallest cluster, and seemed to be mostly younger (18-40) casual local runners (mostly from Massachusetts, especially Boston) with the longest times.
- Cluster 2 was older (40+) casual runners with slightly shorter times across the board than cluster 1.
- Cluster 3 was the largest cluster, and contained the competitive runners of the world from all age ranges, with the shortest run times on average, and more international than the other two clusters (people probably wouldn't travel internationally to compete if they weren't serious).

The 4 cluster model story:
- Cluster 1 was the smallest cluster, and is an older, slower cluster that is mostly male. It represents many runners from Massachusetts. These may be more casual runners as they aren't as fast.
- Cluster 2 has the largest number of participants from most states and most countries. This cluster is younger, more serious runners which, (understandably) makes up the largest group in an internationally renown marathon.
- Cluster 3 is the second fastest, slightly older than cluster 2, and also makes up a large proportion of runners from each country, though there is more variance than cluster 2. This is the complement to cluster 2 and represents the older serious runners of the world.
- Cluster 4 represents young, mostly female, casual/amature runners, many of whom are from Massachusetts/Boston area. It is also a smaller cluster, and seems a complement to cluster 1.

This project was a great example of the power of clustering and unsupervised learning to determine patterns that weren't easily recognizable through univariate and bivariate analysis. I see a lot of potential to use these methods in my feature engineering process moving forward. One poignant example in this case was age, where the algorithm saw a natural separation at 40 among the more casual runners. These kinds of distinctions could be very helpful in making business decisions.
