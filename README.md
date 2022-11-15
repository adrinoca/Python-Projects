# PROYECTOS PYTHON

## Git commands

1. la -ls <- Ver archivos ocultos y normales que hay en el cd
2. git clone <- clonar repositorio
3. git status <- explain the status of the different files.
4. git add <- add files to the staging area
5. git commit -m "Comentario obligatorio" <- commit files to local repository
6. git push origin main <- send coimmited changes of master branch to the remote repository.

## Recommendation Engine

Hay dos tipos de recommendation engines.

### Collaborative Filtering

Collaborative Filtering recommends items based on similarity measures between users and/or items. The basic assumption behind the algorithm is that users with similar interests have common preferences.

Collaborative filtering is based on the idea that similar people (based on the data) generally tend to like similar things. It predicts which item a user will like based on the item preferences of other similar users. 

It uses a user-item matrix to generate recommendations. This matrix contains the values that indicate a user’s preference towards a given item. These values can represent either explicit feedback (direct user ratings) or implicit feedback (indirect user behavior such as listening, purchasing, watching).

1. Explicit Feddback: The amount of data that is collected from the users when they choose to do so. Many of the times, users choose not to provide data for the user. So, this data is scarce and sometimes costs money.  For example, ratings from the user.

2. Implicit Feddback: In implicit feedback, we track user behavior to predict their preference.

Matrix factorization is a way to generate latent features when multiplying two different kinds of entities. Collaborative filtering is the application of matrix factorization to identify the relationship between items’ and users’ entities. With the input of users’ ratings on the shop items, we would like to predict how the users would rate the items so the users can get the recommendation based on the prediction.

$$
UM = U x I
$$

Being the Utility Matrix UM(m x n), Users Matrix U(m x k) and Items Matriz I(k x n).

In real-life scenarios, every user wouldn’t have seen all possible movies. So the rating matrix will look more empty - Sparse Matrix. In this case, the model still learns to factorize the sparse matrix, but RMSE will be calculated only for the ratings that are actually present in the matrix. After obtaining the best factors to approximate the ratings we have, we then perform dot product of the factor matrices to fill in the missing entries in the rating matrix. These filled in ratings are then used to provide recommendations to the users.

### Content-Based Recommendation

It is _supervised machine learning_ used to induce a classifier to discriminate between interesting and uninteresting items for the user. 

In a content-based recommendation system, first, we need to create a profile for each item, which represents the properties of those items. From the user profiles are inferred for a particular user. We use these user profiles to recommend the items to the users from the catalog.

### Ejercico 1. 

Se busca crear un sistema de recomendación colaborativo, es decir, se parte de dos data-sets. El primero contiene los ratings de los usuarios para distintas películas. El segundo está formado por estas películas. Ambos se relacionan por el id de la película.


