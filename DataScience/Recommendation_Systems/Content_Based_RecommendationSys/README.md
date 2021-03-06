# TED Talk Content-Based Recommendation System

![Title Image](https://github.com/yamasjose11/tedtalk-recommendation-system/blob/main/images/tedtalkmainpage.png)

# Motivation and Objective

My motivation for this project is woven in my underlying passion for learning and TED Talks never fail to teach me something new. I want to see if I can replicate what most major streaming services do and that is, see if I can explore and build my very own recommender system. With this in mind, my main focus will be to try and stick to building a content based recommender using various tool and methods to achieve just that.

# Content-Based Recommender System

*A **content-based recommender** looks at the characteristics of the users and items to determine what to recommend. For instance, suppose your open a new MovieBinge account and it asks you for your favorite genres. If you say you like Science Fiction and Comedy, it might recommend Galaxy Quest.*
A content-based approach in our case gives recommendations based on the similarity bewteen different TED Talk attributes. Content-based recommenders are very efficient and very easy to interpret, and are usually great recommenders for new users. 

# The Data

My data is comprised of two datasets from [data.world](https://github.com/yamasjose11/EverythingDataPortfolio/blob/main/DataScience/Recommendation_Systems/Content_Based_RecommendationSys/README.md#references) after joining the datasets I have one dataset that contains over 2,500 offical TED Talk Transcripts up to late 2017. This is where the majority of the text-processing of the data will be conducted to make use of a better translating of a recommender. 

<!-- Word Count Distribution EDA -->
<p align="center">
  <img width="600" height="300" src="https://github.com/yamasjose11/tedtalk-recommendation-system/blob/main/images/doc_word_dist.png">
</p>

# Recommender System Approach

## TF-IDF Recommender

Using TF-IDF is a basic approach that helps us in creating our recommender system by evaluating the corpus and vectorizing it. This is done by using the *Term Frequency* and mulitplying it by the *Inverse of the Document Frequency*. This allows us to focus on the importance of the words used across each document. 

  | Recommendations for *Simon Sinek: How great leaders inspire action* using TF-IDF |
  | --------------------------------------------|
   Seth Godin: How to get your ideas to spread
Scott Dinsmore: How to find work you love
Tony Robbins: Why we do what we do
Ricardo Semler: How to run a company with (almost) no rules
Jeff Hawkins: How brain science will change computing
Michael Norton: How to buy happiness
Yuval Noah Harari: Nationalism vs. globalism: the new political divide
Jessica Jackley: Poverty, money -- and love
Seth Godin: The tribes we lead

After the implementation of the TF-IDF method we see a good recommandations of other TED Talks that revolve around the science of leadership and self development which I believe to be the focal point of the input TED Talk by Simon Sinek.


## LDA Recommender

With the LDA approach we are utilizing topic modeling that allows us the discover nominal "topics" that occur in a collection of documents. In other words, Latent Dirichlet Allocation (LDA) helps us classify our text to a particular "topic" in our baseline LDA model we use the default 10 topics.

  | Recommendations for *Simon Sinek: How great leaders inspire action* using LDA |
  | --------------------------------------------|
John Maeda: How art, technology and design inform creative leaders
Sylvia Earle: My wish: Protect our oceans
Kandice Sumner: How America's public schools keep kids in poverty
David Deutsch: Chemical scum that dream of distant quasars
Colin Camerer: When you're making a deal, what's going on in your brain?
Mona Chalabi: 3 ways to spot a bad statistic
Marvin Minsky: Health and the human mind
Mathias Jud: Art that lets you talk back to NSA spies
Alain de Botton: Atheism 2.0' 'Hans Rosling: New insights on poverty

# Conclusion

Unlike the TF-IDF approach, the suggestions given by the basic LDA approach could be better as some of the recommendations are not very in tune with what I felt were the main focus of the input suggestion by Simon Sinek. So in conclusion the TF-IDF approach has given us more better generic reocmmendations from the choise of TED Talks it decides to return. 

# Future Development

Going forward I would like to expand on this recommender system by making it a hybrid recommender system by combining my current content based recommender system and a newly built collabarative filtering system. This will help me with exploring user personalized recommendations.

# References

Temple, O., 2016. TED Talks- Complete List - dataset by owentemple. [online] Data.world. Available at: <https://data.world/owentemple/ted-talks-complete-list> [Accessed 31 January 2021].
