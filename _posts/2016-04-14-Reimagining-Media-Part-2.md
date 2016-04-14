---
layout: post
title: Reimagining news for the web (Part 1)
---

This post is the second in a two part series that talks about how traditional news companies can reimagine media for the web. The first post outlined 4 areas in which media companies are currently not doing enough. This post suggests solutions to the aforementioned problems.

1. **Use Data Science to personalize offerings to users**: There is a wealth of information that users share with a provider when they visit a site. This includes their IP-address (which can be used to find out their current city), referrer-data (which tells a publisher where a user came from), device data (browser, OS, device type and the like). At the same time, their past browsing history on a site can be tracked and managed with cookies. Yet, publishers typically treat all users the same.

Imagine that you are a shopowner, and you have a customer who always buys apples from you. But apples are stocked all the way at the back of your shop. The customer tries to be loyal for a while, but eventually decides to go to another shop where apples are stocked right at the front.

This analogy is not all that inaccurate for general news publishers that are beginning to lose users to niche sites. Thankfully, Data Science offers a solution. I have implemented a personalized article recommendation system on my site, [TheBroadline.com](http://thebroadline.com). Users are shown articles based on where they live, where they entered the site from, and past articles (if any, that they have seen on the site). For instance, a user living in India who has visited the site for the first time would see the following:
![New Indian User](http://rishsriv.github.io/images/broadline_home_personalization_india.png)

On the contrary, a non-Indian user would see the following:
![New Non-Indian User](http://rishsriv.github.io/images/broadline_home_personalization_usa.png)

Notice how the first recommended article is the only one on my site that is not about India. This is determined automatically determined by algorithms that run round the clock. They look at what users similar to a given user has seen, and recommend articles that a given user might like. I have configured the algorithm to work on a country level (since I have a very limited audience and few articles right now), but you can make it work at a city or regional level as well.

Moreover, if the user has been on the site before, we can hazard a guess at what kind of content she would like. You can use algorithms to then recommend content completely tailored to this user. For instance, after I visited articles about the [role of caste in education in India](http://thebroadline.com/caste-is-not-in-the-past-cbse-class-xii-results.html), and an [increase in communal violence in India](http://thebroadline.com/we-did-the-math-communal-violence-is-indeed-rising-across.html), the algorithm automatically recommended these article the next time I visited the home page:
![Existing User](http://rishsriv.github.io/images/broadline_home_personalization_old_user.png)
