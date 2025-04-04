# AI video reccomendation system
#“Building AI course project”
## Summary

My project will be a video recommendation system. This project aims to develop a Python-based Video Recommendation System that personalizes video suggestions based on user preferences, watch history, and behavior patterns. It does this to improve user experience by providing intelligent and relevant video recommendations, like platforms such as YouTube and Netflix. The recommendation system will use:

- **Content-based filtering**: Analyzes the video's metadata (titles, descriptions, tags) to suggest similar content.
- **Collaborative filtering**: Uses user interactions (watch time, likes, and ratings) to identify patterns among users with similar interests.

Combining both methods may also be used to improve accuracy.

## Background

The recommendation system aims to solve several problems related to content discovery and user engagement:

* **Problem 1**: Users are overwhelmed with irrelevant or repetitive content suggestions on video platforms.
* **Problem 2**: Traditional recommendation engines fail to understand and anticipate individual user preferences, leading to unsatisfactory user experiences.
* **Problem 3**: Users often spend too much time searching for new and engaging content.

This is important because it can vastly improve the user experience on platforms like YouTube, Netflix, and educational websites, where discovering relevant content quickly is crucial.

## How is it used?
![image](https://github.com/user-attachments/assets/fc329b76-7ac0-4e38-b720-e535403955af)

The system is designed to be integrated into video streaming platforms, where it will provide personalized video suggestions for users based on their past interactions.
**Usage Process**:
1. **User Interaction**: The system tracks videos the user has watched, liked, or rated.
2. **Algorithm Processing**: Using these data points, the system analyzes content preferences, leveraging content-based filtering and collaborative filtering.
3. **Personalized Suggestions**: Based on the analysis, the system provides tailored video recommendations.

**Potential Use Cases**:
- **Entertainment**: Platforms like YouTube and Netflix could benefit from personalized content suggestions.
- **Education**: Recommend educational videos based on user interest or learning goals.
- **Social Media**: Suggest viral or trending content based on user activity.


## Example of Code:
import math
import random
import numpy as np
import io
from io import StringIO
import numpy as np

x_train = np.random.rand(10, 3)   # generate 10 random vectors of dimension 3
x_test = np.random.rand(3)        # generate one more random vector of the same dimension

def dist(a, b):
    sum = 0
    for ai, bi in zip(a, b):
        sum = sum + (ai - bi)**2
    return np.sqrt(sum)
    
def nearest(x_train, x_test):
    nearest = -1
    min_distance = np.Inf
    # add a loop here that goes through all the vectors in x_train and finds the one that
    # is nearest to x_test. return the index (between 0, ..., len(x_train)-1) of the nearest
    # neighbor
    for x in range(len(x_train)):
        # Compute the distance between x_test and the current training vector
        distance = dist(x_train[x], x_test)
        # If the current distance is smaller than the minimum distance, update
        if distance<min_distance:
            min_distance=distance
            nearest = x  # Store the index of the nearest vector
    print(nearest)

nearest(x_train, x_test)




#this code is similar to the code i will be using in my algorithm as it uses similar shapes. this code could be an analogy of finding similar videos to the previous video just watched etc.
