# CROSS-GENRE RECOMMENDER ENGINE

Much progressive work in recommender engine research has been focused on applying recommendation algorithms across heterogeneous domains. Logic may be abstracted so that the formulas generating suggestions for what books a user might like to read can be utilized in similar fashion to suggest stage plays to experience or home appliances to buy, as well what automobiles fit the consumer's personality and what desserts the user may want to indulge upon. While we can apply techniques between unrelted industries, I've not found a great deal of work of **cross-genre recommendations**, such that content within the same industry - in this case, movies - can be used as a basis for recommending films a user might enjoy from categories that at face value they probably shun because of their aggregate unappeal.


### DESCRIPTION

We all have patterns in our preferences. If you tend to watch a lot of cerebral documentaries, there's a fair chance you're not into stoner comedies. Fans of 80s slasher horror cinema don't always dig musicals. Animated super hero flicks may not necessarily jive with people into apocalyptic science-fiction. If religious movies are your passion, you're probably not a purveyor of hardcore porn. If you frequent sports dramas, you might not be a legal trial film buff. You get the idea. But there are some golden opportunities that may be missed because of this overall bias on principle.

We all very happily slip into patterns and can get trapped in our corners. This isn't an attempt to broaden your horizon or extend your coverage, merely to provide a conduit to neat to content you'd likely see as interesting but normally never find.


### MOTIVATION

This project attempts to construct algorithms that examine the latent characteristics of the films in a user's viewed history, and propose films in disparate genres to allow them to discover new content they might enjoy. The theory behind it all is that a certain amount of natural hidden characteristics are shared between users and items, even if they aren't consciously aware of them. It's the same phenomenon driving attraction between people, just less obvious. The key is how many characteristics are shared, and to what degree. By examining what's essentially the "DNA" of the user's consumption patterns, I believe we can find a set of items that will be intriguing to a user's tastes - even if she doesn't agree with the overall grouping.


### DATASETS

This project uses the free datasets from [MovieLens](http://grouplens.org/datasets/movielens/20m/) and [IMDb](http://www.imdb.com/interfaces), cross-referenced to setup general categorizations for movies.


### METHODOLOGY

Computing such recommendations requires certain proven techniques.

- A hybrid of [content-based filtering](http://recommender-systems.org/content-based-filtering/) and [item-item collaborative filtering](https://en.wikipedia.org/wiki/Item-item_collaborative_filtering)
- [Latent Dirichlet Allocation](https://en.wikipedia.org/wiki/Latent_Dirichlet_allocation) and [latent factor modeling](http://www.ideal.ece.utexas.edu/seminar/LatentFactorModels.pdf) to identify the hidden relations between the user's selections and items in the library


### CHALLENGES

The difficult thing herein is the lack of a concrete **explanation** of the recommendations, which is [typically a key component](https://pdfs.semanticscholar.org/4adc/c5d7429adcea3b365a223fac2441880cab28.pdf) in the overall user interface of an effective recommender system. Because the latent factors aren't easily discernible for humans, if at all, being low-level mathematics relations, it's complicated to relay to the end user why a certain movie was suggested. This should require a new way to reinforce the ranking, as items don't intuitively pass the eyetest for why they're being recommended.
