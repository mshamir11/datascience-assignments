# Assignment 1 ⭐ <!-- omit in toc -->


## Contents 📑 <!-- omit in toc -->
- [Problem 1](#problem-1)
- [Problem 2](#problem-2)
- [Problem 3](#problem-3)
- [Problem 4 💰](#problem-4-)
  - [Greedy Method Algorithm](#greedy-method-algorithm)
  - [Results](#results)
- [Problem 5](#problem-5)





### Problem 1
### Problem 2
### Problem 3

### Problem 4 💰

Download the dataset in <https://www.kaggle.com/arjunbhasin2013/ccdata./> As a good practice, normalize each feature such that the values are all in the range [0, 1]. Treat the CUST ID column as the identity of the point, not a feature. Use the L2 metric as distance. Implement the greedy k-center algorithm for this data and report the k-center objective value for k = 2, 4, 10. For small values of k, say k =2, 4 , find the optimal (when the centers are restricted to be input points) and report the approximation factor obtained by the greedy algorithm.

**Solution**

#### Greedy Method Algorithm

Pseudo Code to find K centers:

Choose randomly a center from the given input point. Say the first point. and the input list be X.

```python
center_list = []      


distance_array =[INF]*len(X)

for i in range(K):
    current_center = select the point in X which has the maximum distance from all the centers (basically the one with max value in the distance_array)
    cluster_radius = {}
    center_list.add(current_center)
    
    for point in X:

        d = distance(point,c)
        distance_array[point] = min(distance_array[point],d) // Update the distance_array. 

        cluster_radius = max(distance_array[point],cluser_radius)
        
    cluster_radius[current_center] = cluster_radius

```

**To find the most optimal one**, the first k-center needs to be optimized. Earlier we had selected it randomly. Now, we would find the objective function for all the input points as first and the final objective value would be the minimum among all the k-centers chosen.

#### Results


### Problem 5

