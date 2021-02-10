# Assignment 1 ⭐ <!-- omit in toc -->


## Contents 📑 <!-- omit in toc -->
- [Problem 1](#problem-1)
- [Problem 2](#problem-2)
- [Problem 3](#problem-3)
- [Problem 4 💰](#problem-4-)
  - [Greedy Method Algorithm](#greedy-method-algorithm)
  - [Link to the Solution Notebook](#link-to-the-solution-notebook)
  - [Results 🌟](#results-)
- [Problem 5](#problem-5)





### Problem 1
 Is the following function d(x, y) = mini
|xi − yi| a metric? Either prove it or give counter-examples.

**Solution**
Let's check whether the function follows the metric properties.

1. d(x,x) =0    
   Here, min |xi - xi| =0. Therefore it satisfies that property.

2. d(x,y) = d(y,x)  
   |yi - xi| = |xi - yi|    
   min |yi - xi| = min |xi - yi|   
   d(y,x) = d(x,y)
   It satisfies this property also.

3. d(x,y) + d(y,z) <= d(x,z)
   
   $\begin{bmatrix}a & b\\c & d\end{bmatrix}$

### Problem 2
### Problem 3

### Problem 4 💰

Download the dataset in <https://www.kaggle.com/arjunbhasin2013/ccdata./> As a good practice, normalize each feature such that the values are all in the range [0, 1]. Treat the CUST ID column as the identity of the point, not a feature. Use the L2 metric as distance. Implement the greedy k-center algorithm for this data and report the k-center objective value for k = 2, 4, 10. For small values of k, say k =2, 4 , find the optimal (when the centers are restricted to be input points) and report the approximation factor obtained by the greedy algorithm.

**Solution** 💡 

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

#### [Link to the Solution Notebook](https://nbviewer.jupyter.org/github/mshamir11/datascience-assignments/blob/master/Assignments%201/4/question_4.ipynb#first-bullet)

#### Results 🌟

- The Approximation Factor is coming about to be **1.3966834349636552** for **k=2** and **1.4667634183920994** for **k=4**.
- Theoretically the Approximation Factor should be less than or equal to 2.
- The Truthness of the Approximation Factor is validated using this experiment.

### Problem 5
For the following question you need to submit a link to a recorded video, YouTube link is preferable (can
be unlisted). We intend to link to these videos from our public course webpage.

Go through the video at https://www.youtube.com/watch?v=hVimVzgtD6w. There are number of li-
braries to create such visualization: one example is GapMinder animation, another is Plotly. Choose any dataset from any of the following websites:   

- https://www.gapminder.org/data/
- http://www.healthdata.org/data-visualization/gbd-compare or http://ghdx.healthdata.org/
gbd-2017 (in Select Articles there are folder with data).
- https://niti.gov.in/state-statistics.
- 
Take any two parameters, and either a number of Indian states, or a number of countries including India.
Then create such a visualization. We rely on you to choose two parameters that make a somewhat
interesting story as Hans Rosling does. If you want to use datasets about pandemic that is also fine —
either come up with suggestions, or reach out to us.
Note that you have to be sometimes careful about missing data, data formatting etc these are all part of
the problem. Document what problems you faced and what you did to handle these.

**Solution**

The data were taken from <https://www.gapminder.org/data/>