# 😄 Jester Joke Rating Collaborative Filtering

## 💼 Business use case

Personalized feeds benefit from predicting what a user may enjoy before they have rated every item. Humor is a useful stress test for collaborative filtering because preferences are highly subjective and direct content features can be difficult to engineer.

## 🎯 Principal objective

Build a sparse user-joke rating matrix, hide part of the observed feedback, and apply SoftImpute collaborative filtering to recover likely ratings. The model is evaluated against an average-rating baseline using in-sample and out-of-sample R².

## 🔎 Summary of takeaways

The stored run reaches **0.3463 out-of-sample R²** and **0.5143 in-sample R²**. Among the three matrix-completion projects in this portfolio set, this notebook has the strongest validation R² and a smaller train-validation gap than the MovieLens experiment.

The result suggests that shared taste patterns can support useful personalization even for subjective content. A production recommender would still need ranking-based evaluation, cold-start handling, exploration, and possibly hybrid features rather than relying on rating reconstruction alone.

## 🧭 Explore the code

Open the [notebook](https://github.com/saels/jester-joke-rating-collaborative-filtering/blob/f5a7796d92796de14becb4b28eba9172c44a3139/Jester_joke_rating_collaborative_filtering.ipynb) to see how the sparse ratings are prepared, masked, completed, and scored. The code provides a clean comparison point for understanding how the same collaborative-filtering method behaves on a different preference domain.
