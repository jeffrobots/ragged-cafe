# high level goal

Given a query about what kind of coffee you want, recommend 1-2 coffee options.
Return data about the rating, and explain why it's a good match.


1. Initially just based on review
2. Could also incorporate cost later (weighting function?)
3. How should I increase the size of this dataset?



# Approach

1. Tokenize all reviews
2. Accept input query
3. Tokenize query
4. Perform KNN lookup for reviews
5. submit top-k and use a lightweight language model to choose the best with explanation.


This dataset is small, so we can probably put everything into a local database no problem.
Let's focus on scale later.
We can also probably get away with pre-computing all of our encoding/tokens regardless of how expensive that operation is. That would scale well, but it's also not difficult.

6. For other metadata, we can start to fold it in later. IE KNN lookups with multiple parameters.

