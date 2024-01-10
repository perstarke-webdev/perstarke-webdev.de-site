---
title: "Recipe Recommender - My Bachelor Thesis"
permalink: /posts/bachelorthesis-recipe-recommender
layout: single
excerpt: "I wrote my Bachelor Thesis about algorithms for personalized recipe recommendations - here are some insights!"
---

## Summary

My bachelor thesis investigated the effectiveness of algorithms for personalized recipe recommendations. 
The research tested whether _collaborative filtering_ or _content-based_ approaches yield more satisfying results in terms of matching users' taste. 
To achieve this, a software application was developed, implementing both _ItemKNN_ and _content-based algorithm_,allowing for a direct comparison of their recommendation outcomes.

The evaluation of these algorithms was performed using a database containing more than 1000 recipes plus recommendation and rating information
. 
The results obtained from this software provided valuable insights into the effectiveness of both algorithms in the context of recipe recommendations. 

>Analyzing these results revealed a statistically significant difference in user ratings, with the ItemKNN algorithm receiving higher average ratings (4.2 out of 5 stars) compared to the content-based algorithm (3.389 stars). 
>This suggests that, on average, users found the recommendations provided by the ItemKNN algorithm more appealing and satisfying
>The study thus underlines the effectiveness of collaborative filtering approaches in the context of personalized recipe recommendations.

Thanx to Prof. Tobias Thelen and the University of Osnabrück for supporting this work.

## Software architecture

The architecture of the Recipe Recommender system was documented with parts of the
[arc42 software architecture documentation template](https://arc42.org/).  

I used the [arc42 Architecture Communication Canvas](https://canvas.arc42.org/architecture-communication-canvas)
to give a brief overview of the software architecture.  
The canvas for the Recipe Recommender can be found below.  
More details can be found here soon.

<figure>

    <div class="image-container">
      
        <a href="/images/posts/ba/acc-RecipeRecommender-1920px.webp" title="Architecture Communication Canvas for the Recipe Recommender system">
          <img src="/images/posts/ba/acc-RecipeRecommender-1920px.webp" alt="Architecture Communication Canvas for the Recipe Recommender system" />
        </a>

    </div>

</figure>