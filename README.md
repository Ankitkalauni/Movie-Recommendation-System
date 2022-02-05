# Content-Based Movie Recommendation System

## CHAPTER 1: INTRODUCTION

### Background:
As the World Wide Web continues to grow at an exponential rate, the size and complexity of certain data or web site grow along with it. For the users of these websites, it becomes increasingly difficult and time-consuming to find the information they are looking for. To help users find the information that is in accordance with their interests a website can be personalized. Recommender systems can improve a website for individual users by dynamically adding “relevant” information.

When users browse through a website they are usually looking for items they find interesting. Interest items can consist of a number of things. For example, movie information can be considered as interest items.

Every large collection needs a certain structure to make it easy for visitors to find what they are looking for. A website can be structured by dividing its web pages into content pages and navigation pages. The content pages provide the user with the interest items while the navigation pages help the user to search for the interest items.

One popular technique of recommendation/recommender systems is content-based filtering. Content here refers to the content or attributes of the products you like. So, the idea in content-based filtering is to tag products using certain keywords, understand what the user likes, look up those keywords in the database and recommend different products with the same attributes.


### **Abstract:**
In this fast and complex world, several alternatives of products are available for a given product. Think of the examples above: streaming videos, social networking, online shopping. the list goes on. Recommendation systems help to personalize a platform and help the user find something they like.

Machine learning algorithms in recommender systems typically fit into two categories: content-based systems and collaborative filtering systems. Modern recommender systems combine both approaches. A content-Based Recommendation system is used to suggest “relevant” items to users. They predict future behaviour based on past data. Content-based methods are based on the similarity of movie attributes. Using this type of recommender system, if a user watches one movie, similar movies are recommended.

From a business standpoint, the more relevant products a user finds on the platform, the higher their engagement. This often results in increased revenue for the platform itself. Various sources say that as much as 35–40% of a tech giant’s revenue comes from recommendations alone.


### **Objective:**
* Web-based application of content recommendation system, will show the searched movie information and recommend relevant movies to get the information about that movie
* Users can search for a movie and get information about the movies casts, trivia, descriptions, reviews
* Users can add reviews and upvote or downvote particular movies.

* No hard-coding in the system, simple code structure and pseudo code

* Easy to update and modify the new data into the system using Machine Learning Pipeline

* Deploy recommendation system once and use multiple times, even on unseen new data. ie. on new movies


### Purpose:
A recommendation system helps the user to find useful and relevant information from the website which also increase user engagement on the website. It helps users find compelling content in large corpora. For example, the Google Play Store provides millions of apps, while YouTube provides billions of videos. More apps and videos are added every day. How can users find new compelling new content? Yes, one can use search to access the content. However, a recommendation engine can display items that users might not have thought to search for on their own.


### Scope:
The recommendation system overcomes the idea of the hard-coded sites, which makes lots of loads in work and increases the breakdown of the websites as the hard-coded website needed to be updated frequently. On the other side websites which use Recommendation Systems can train the machine learning model once and use it as many times as it wants. it also works if the websites get updated. As if new movies were added to the website database. The developer can make the machine learning pipeline to preprocess a new dataset with one click. This will decrease the workload and make the system more efficient and faster.


### Applicability:
The recommendation system filters out the information automatically for the user, so they do not have to search for it explicitly. Users can get the related article, information with a single click. They can find the information which cant find directly from the searched term. This will increase the engagement of the user on the website, and users can explore the website and get the needed information, the applicability of this recommendation system is that it overcomes the old traditional website which uses hardcoding. Machine learning recommendation system has a simple data structure and can be easily modified and update, updating this recommendation system make it smarter on the basis of information.


### Achievements:
* In this project(Content-based recommendation system ) we can achieve some benefits, which are listed below.
* Recommend relevant movies related to the searched movies on the navigation page
* Train model once and use it many times
* No hard-coding, the model can predict new movies which are added into the website database
* Easy to update Recommendation system without taking down the server
* Add reviews of the new users on the website and Recommendation system


## CHAPTER 2: SURVEY OF TECHNOLOGIES

### 2.1 Technologies used in the frontend with all features.

    2.1.1 We have taken HTML, CSS, JavaScript & Bootstrap for the front-end website development.
    2.1.2 Feature of HTML & CSS
It is easy to learn and easy to use.
It is platform-independent.
Images, videos, and audio can be added to a web page.
Hypertext can be added to the text.
It is a markup language.
CSS allows users to view documents with their own preferred fonts, colors, etc. by specifying them in a user style sheet.
 
     2.1.3 Feature of JavaScript
Light Weight Scripting language.
Dynamic Typing.
Object-oriented programming support.
Functional Style.
Platform Independent.
Prototype-based.
Interpreted Language.
 
     2.1.4 Feature of Bootstrap.
Fewer Cross-browser bugs
A consistent framework that supports major of all browsers and CSS compatibility fixes
Lightweight and customizable
Responsive structures and styles
Several JavaScript plugins using the jQuery
Good documentation and community support
Loads of free and professional templates, WordPress themes and plugins
 
### 2.2 Technologies used in the backend with all features.
    2.2.1 We have taken Flask for framework and Pickle to save trained machine learning model
    2.2.2 Features of Flask.
It is very flexible and easy to learn
It provides unit testing through its integrated support, built-in development server, fast debugger and restful request dispatching
It is a lightweight framework so it is fast.
    2.2.3 Features of Pickel.
Pickle is the standard way of serializing objects in Python. You can use the pickle operation to serialize your machine learning algorithms and save the serialized format to a file.
Later you can load this file to deserialize your model and use it to make new predictions.
### 2.3 Comparative Technologies of Project
	2.3.1 Django
Django is a web development framework for Python. This framework offers a standard method for fast and effective website development. It helps you in building and maintaining quality web applications. It enables you to make the development process smooth and time-saving.
 
Flask is a micro-framework offering basic features of the web app. This framework has no dependencies on external libraries. The framework offers extensions for form validation, object-relational mappers, open authentication systems, uploading mechanism, and several other tools.
 
Flask is a good choice if you want a lightweight codebase. The best feature of Django is Robust documentation. Flask framework is suitable for single applications. Django framework allows developers to divide a project into multiple page application

### DataFlow Diagram.

Level 0:

![Image of DataFlow Diagram level 0](https://github.com/Ankitkalauni/Movie-Recommendation-System/blob/main/Images/DFD_0_Movie_recommendation_system.png?raw=true)

Level 1:

![Image of DataFlow Diagram level 1](https://github.com/Ankitkalauni/Movie-Recommendation-System/blob/main/Images/DFD_1_Movie_recommendation_system.png?raw=true)


___
<a name='3'></a>
## 3 - Cosine Similarity

To measure the similarity between two words, you need a way to measure the degree of similarity between two embedding vectors for the two words. Given two vectors $u$ and $v$, cosine similarity is defined as follows: 

$$\text{CosineSimilarity(u, v)} = \frac {u \cdot v} {||u||_2 ||v||_2} = cos(\theta) \tag{1}$$

* $u \cdot v$ is the dot product (or inner product) of two vectors
* $||u||_2$ is the norm (or length) of the vector $u$
* $\theta$ is the angle between $u$ and $v$. 
* The cosine similarity depends on the angle between $u$ and $v$. 
    * If $u$ and $v$ are very similar, their cosine similarity will be close to 1.
    * If they are dissimilar, the cosine similarity will take a smaller value. 

<img src="https://github.com/Ankitkalauni/Movie-Recommendation-System/blob/main/Images/cosine_sim.png?raw=true" style="width:800px;height:250px;">
<caption><center><font color='purple'><b>Figure 1</b>: The cosine of the angle between two vectors is a measure of their similarity.</font></center></caption>
