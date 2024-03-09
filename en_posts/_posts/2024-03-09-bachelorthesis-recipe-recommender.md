---
title: "Recipe Recommender - My Bachelor Thesis"
permalink: /posts/en/bachelorthesis-recipe-recommender
layout: single_en
excerpt: "I wrote my Bachelor Thesis about algorithms for personalized recipe recommendations - here are some insights!"
---

## Summary

My bachelor thesis investigated the effectiveness of algorithms for personalized recipe recommendations. 
The research tested whether _collaborative filtering_ or _content-based_ approaches yield more satisfying results in terms of matching users' taste. 
To achieve this, a software application was developed, implementing both an _ItemKNN_ and a _content-based algorithm_, allowing for a direct comparison of their recommendation outcomes.

The evaluation of these algorithms was performed using a database containing more than 1000 recipes plus recommendation and rating information. 
The results obtained from this software provided valuable insights into the effectiveness of both algorithms in the context of recipe recommendations. 

>Analyzing these results revealed a statistically significant difference in user ratings, with the ItemKNN algorithm receiving higher average ratings (4.2 out of 5 stars) compared to the content-based algorithm (3.389 stars). 
>This suggests that, on average, users found the recommendations provided by the ItemKNN algorithm more appealing and satisfying.
>The study thus underlines the effectiveness of collaborative filtering approaches in the context of personalized recipe recommendations.

Thanx to Prof. Tobias Thelen and the University of Osnabrück for supporting this work.

## Background 

Recommender systems are like personal assistants in the digital world, 
helping you find things you might like. The most famous example here is Netflix with its personalized series/movies recommendations.

They come in two main types:
***collaborative filtering***, which looks at what you and others have liked before, 
and ***content-based***, which focuses on the details of the items themselves. 
For example, in recipe recommendations, 
collaborative filtering might consider what recipes people with similar tastes enjoyed, 
while content-based methods look at the ingredients and flavors. 
These systems are also super useful in areas like nutrition coaching for athletes, 
where personalized meal plans can make a big difference. 
Figuring out which method works best is key to making recommendations that really hit the spot for users.

## Finding out which algorithm works best
To get an idea of which algorithm works best in the realm of personalized recipe recommendations, 
I implemented a web application, which offered personalized recommendations for users.  
This software applied both types of algorithms, to directly compare them.  
A study with volunteer users then gave insights into the performance of both types of algorithms in the context of recipe recommendations.

## Software functionality
The web application offered both users and coaches a comprehensive set of functionalities, 
with a primary focus on accessing personalized recipe recommendations. 
Users could log in or create accounts to explore tailored suggestions, rate recipes, and enter dietary preferences. 
Coaches, on the other hand, could manage clients, send coaching requests, 
and access client accounts to provide personalized recommendations.
Additionally, a [documentation video](https://www.youtube.com/watch?v=OnRLb6I9Www) offered users a detailed tutorial on how to navigate the platform and 
make the most of its recommendation features.

## Software architecture

The architecture of the Recipe Recommender system was documented with parts of the
[arc42 software architecture documentation template](https://arc42.org/).  

I used the [arc42 Architecture Communication Canvas](https://canvas.arc42.org/architecture-communication-canvas)
to give a brief overview of the software architecture.  
The canvas for the Recipe Recommender can be found below.

<figure>

    <div class="image-container">
      
        <a href="/images/posts/ba/acc-RecipeRecommender-1920px.webp" title="Architecture Communication Canvas for the Recipe Recommender system">
          <img src="/images/posts/ba/acc-RecipeRecommender-1920px.webp" alt="Architecture Communication Canvas for the Recipe Recommender system" />
        </a>

    </div>

</figure>

#### Operation phases

Five distinct operation phases can be differentiated. These are:
- Phase 1: Create the recipe database,
- phase 2: calculate and write the recipe similarities,
- phase 3: get initial ratings,
- phase 4: users & coaches use the software and
- phase 5: evaluation.

Phase 1 to phase 3 served as initialization phases. 
They provided the foundation for the core phase 4, 
where users and coaches engaged with the software to receive personalized recipe recommendations. 
Phase 5 was started during phase 4, when users got and rated recommended recipes, 
with these ratings stored in a CSV file instead of a relational database for simplicity. 
When enough ratings had been collected in this file, the evaluation could take place, 
providing the necessary results to discuss and answer the research question. 

#### Solution strategy / tech-stack

I chose Python as the primary programming language due to its widespread usage, clean syntax, and versatility in web development and data analysis.

Several Python libraries were utilized:
- [Flask](https://flask.palletsprojects.com/en/3.0.x/) for deploying the system as a web application.
- [Pandas](https://pandas.pydata.org/) for data manipulation and analysis.
- [CaseRecommender](https://github.com/caserec/CaseRecommender) for recommendation algorithms.
- The [Spoonacular API](https://spoonacular.com/food-api) for accessing recipe-related data.

Flask facilitated easy user access to the system as a web application.

HTML and CSS were employed for website structure and design.  
With my knowledge from today, I probably would have used a Javascript frontend library like Quasar instead of just raw HTML and CSS, 
I believe that could have made the development process smoother and offered even better usability.

Pandas played a vital role in cleaning and processing the data, utilizing its DataFrame structure for efficient storage and manipulation.

The CaseRecommender library provided implementations of recommendation algorithms for comparative evaluation.

The Spoonacular API enriched the system with recipe-related data and functions, contributing to the creation of a comprehensive recipe database.


## Limitations 

While the developed software proved valuable for recipe recommendations and addressing the research question, it's important to acknowledge its limitations, which were discussed in the thesis but not addressed in the software due to the scope of a bachelor thesis.

Key limitations include:

- **Limited functionality**: Users cannot specify allergies or dietary restrictions, limiting the software's adaptability to individual needs.

- **Algorithm variability**: Different versions of each algorithm type may yield varying performance results, impacting the accuracy of recommendations.

- **Recipe similarity calculation**: The content-based algorithm includes a recipe similarity calculation developed in-house, which has not been validated against benchmark datasets. 
  Consequently, the use of a different similarity calculation method may lead to disparate recommendation outcomes.

By recognizing these limitations, future research can address these challenges and enhance user experience and recommendation accuracy.

## Conclusion
In this era of technology and data, 
ongoing research in this field remains essential. 
The insights from this study can serve as a foundation for future projects. 
By addressing the limitations of this research and building upon its insights, 
we can look forward to a future of even more sophisticated and user-centric 
recommendation algorithms for personalized recipe recommendations. 
This thesis marks a step toward that goal.


