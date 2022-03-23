Two kinds of recommendations are commonly used:
- home page recommendations (caps project)(A. Personalized Content: Helps to Improve the on-site experience by creating dynamic recommendations for different kinds of audiences like Netflix does)
- related item recommendations (B. Better Product search experience: Helps to categories the product based on their features. Eg: Material, Season, etc.)

    “40% of app installs on Google Play come from recommendations.
    60% of watch time on YouTube comes from recommendations.
    amazon’s 35% of the revenue comes from these recommendation engines”

Embedding
A mapping from a discrete set (in this case, the set of queries, or the set of items to recommend) to a vector space called the embedding space. Many recommendation systems rely on learning an appropriate embedding representation of the queries and items.

One common architecture for recommendation systems consists of the following components:
- candidate generation
  we first used content-based & collaborative filtering for candidate generation.
  content-based pros easier to scale to a large number of users/ can recommend niche items 
  content-based cons requires a lot of domain knowledge to hand-engineer features, cannot expand on the users' existing interests
  user based collaborative filtering
  item based collaborative filtering
- scoring
- re-ranking --- 如果user specifically dislike了谁，或者boost买了ads位的，etc.


Embedding Space captures some latent structure of the item or query set

this is so cool loll http://projector.tensorflow.org/

Comparing Similarity Measures
- cosine
- dot product: norm = popularity
- Euclidean distance

Items that appear very rarely may not be updated frequently during training. Consequently, if they are initialized with a large norm, the system may recommend rare items over more relevant items. To avoid this problem, be careful about embedding initialization, and use appropriate regularization. We will detail this problem in the first exercise.

