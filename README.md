# Yelp_CRM_NLP
The goal of this capstone project is responding negative reviews in real-time so as to improve customer satisfaction. 
Using the Yelp Open Dataset published on September 1, 2017 as our dataset, we conducted sentiment analysis by NLTK package to separate positive and negative reviews. To attain our goal, complaints were selected exclusively as the corpus. Then, we utilized the spaCy package to preprocess the complaint reviews, and the gensim package to train n-gram phrase models and Latent Dirichlet Allocation (LDA) topic models. Finally, we built an automated Telegram chatbot to demonstrate the replies to different types of complaints. There are some interesting insights found in this project:

(1) We calculated the difference between the number of stars given for each review and that reviewer’s average star rating across all reviews. The result yields a column named star difference (“stars_dif”). There is a large concentration at zero star difference, which suggests that many users give the exact same rating for every review. Thus, the value of review stars is questionable for sentiment classification. This motivates us to further conduct sentiment analysis.

(2) Even a 5-star rated review can be a negative review based on our sentiment analysis.

(3) According to the LDA topic model, the three complaint categories include price, food quality, and service quality. The most problematic issue is service quality.

(4) There are 18749 restaurants are categorized as negative rated dining places. 3677 restaurants are in Arizona, Nevada, and California.

(5) The chatbot currently responds with a single reply to the most prominent topic. However, sometimes, customer complaints are mixed problems. We can further improve the chatbot to reply with an appropriate response incorporating multiple solutions. Additionally, the accuracy of the result depends on the volume of the text. Therefore, creating a common word database and tagging those words into certain categories may improve the performance.

We made a Shiny app to visulize the distribution of restaurants, LDA, and chatbot. If you would like to know more about the workflow, concepts, and insights, please feel free to check out our blog post. https://blog.nycdatascience.com/student-works/capstone/real-time-yelp-reviews-analysis-response-solutions-restaurant-owners/
Slides
https://docs.google.com/presentation/d/1QP6qXirIbS6aCRvcUr1oJglEin3FVzJ5sI9aCQQs-cs/edit?usp=sharing
