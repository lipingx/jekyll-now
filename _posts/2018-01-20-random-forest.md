Why Use Decision Trees?linkmode_edit
Why use a decision tree model to fit the YouTube data? Decision trees have four distinctive abilities that are assets in developing our YouTube quality classifier:

Decision trees can model nonlinearities. Unlike logistic regression, which fits a linear equation to data and can only model nonlinear relationships through feature engineering (e.g., feature crosses), decision tree models are represented mathematically as step functions, and are designed to approximate all manner of nonlinear functions.

Decision trees are highly interpretable. Neural networks are also designed to model nonlinearities (via activation functions on hidden layers). However, their predictions can be very difficult to interpret; the significance of a given node weight's contribution to the result is often opaque. Answering the question, "Why did the classifier predict high-quality for Video A and low-quality for Video B" is invaluable for model debugging. If a decision tree misclassifies a video, it's relatively easy to reverse-engineer the result; we perform a "traceback" on the tree, following the path backward to identify the logic that proved problematic. For example:

"The model predicted low-quality here, because views is < 1,000 and average_rating is 2. However, it failed to take into account that this video is new (only 3 days old, with only one user rating), which makes its low scores on view/rating metrics less predictive of quality."

Decision trees do not require extensive feature preprocessing. Trees work well in cases where data comprises multiple features at different scales, or contains missing values. Compared to linear models, they require relatively little data normalization.

Decision trees do not require enormous data sets. Provided features are dense, decision trees perform well on small-to-medium-sized data sets, containing 1K to 10MM examples. Here, we're using a data set with 13,564 examples, which falls right in this range.


