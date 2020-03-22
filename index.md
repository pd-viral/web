---
layout: page
title: Positive Deviance goes Viral
tagline: Using data and local solutions against Corona
description: A Data-Driven Approach to Finding Positive Deviants in the Corona Crisis
---

![headerimg](/img/logo.png){:class="img-responsive"} 



# Corona is affecting everyone - from a global to a local level!
The corona crisis is unfolding worldwide: States, municipalities, villages, and citizens are facing unprecedented, existential challenges. Corona is a global crisis, that does not stop at border checkpoints and has been deeply affecting our everyday live. No global crisis in modern history has been so closely monitored with data. The access to dashboards and other data visualizations show us almost in real time the cruel reality of a quickly spreading pandemic within a globalized world. 

At the same time, the huge quantity of data on this outbreak allows us to gain valuable insights on how to best tackle the negative consequences COVID-19 has on our lives. Scientists, politicians and civil society are coming closer to develop data-driven solutions. We want to contribute to this effort and have come together as individuals from diverse backgrounds and professions to join forces in analyzing the data available and identifying what we call the “positive deviants”. 

# Identifying Positive Deviance: Local Solutions for Global Challenges
Positive Deviants are individuals, groups, cities, regions etc. who outperform their peers in a comparable context thanks to creative and highly adaptive solutions they have come up with. These solutions have proven to work in a specific context and offer as such a high potential to support their peers facing the same challenges. The Positive Deviance approach was first developed in the 1990s by Sternin and Sternin on child nutrition in Vietnam [Pascale, Sternin and Sternin (2010)](https://books.google.de/books/about/The_Power_Of_Positive_Deviance.html?id=nBgDmcy9SnkC&redir_esc=y "Pascale, Sternin and Sternin (2010)"). [Albanna and Heeks (2018)](https://onlinelibrary.wiley.com/doi/full/10.1002/isd2.12063 "Albanna and Heeks (2018)") have looked into the possibility of identifying positive deviants through the analysis of big data, e.g. identifying rice farmers through satellite imagery who manage to produce significantly higher yields than their peers. Solutions developed by Positive Deviants are so effective as they are locally developed, highly context-sensitive, and usually involve a great level of ownership by their communities. Regarding the huge challenges we are facing as local communities, we believe that the positive deviance approach has a great potential to help counties and municipalities in tackling the devastating consequences of the corona outbreak.  

# Applying the Positive Deviance approach to tackle the Corona crisis
While most communities are experiencing existential challenges through the corona outbreak, some communities are more successful in facing them than others, despite facing similar circumstances. **The objective of this challenge is to find and learn from them!**

We believe that understanding how communities deal with the outbreak and find solutions they have come up with, can effectively support existing efforts to deal with the Corona outbreak. 
Therefore our objective is to identify those communities who have managed to deal better with COVID-19 than others - our “Positive Deviants”.

On our endeavour to identify those communities, we a.) need to make communities comparable. Therefore, we statistically control for a wide range of structural variables - such as population density, hospital beds or age distribution. This allows us to cluster those counties and municipalities with similar resources and structural conditions. Based on an analysis of this cluster, we b.) might be able to identify structural conditions who could have a correlation with the spread of the virus. However more than anything we are c.) striving to identify communities that outperform others in dealing with Covid-19 - **independently** from accessible resources or other structural conditions, but thanks to their behaviour and specific solutions. 

# Analysis
![Structure](img/structure.png){:class="img-responsive"}

## Our Methodology
As the Coronavirus spreads, the number of infected people grows exponentially. In all countries, infected people infect others, who themselves can infect more people. This pattern can also be observed within the individual districts (Landkreise/Kreisfreie Städte) within Germany. **We try to identify those districts, where the virus spreads relatively slowly compared to other districts. We first statistically control for any structural influence on this performance and then identify the districts that are outperforming other districts based on unusual behaviors:  Positive Deviants.** Using open source data, we aim to find connections between district characteristics on the one hand, and infection speed on the other hand. 

## 1. Gathering the data
In a first step, **we use data on structural factors, such as the number of doctors, hospitals, academic workers, or unemployment ratio which we retrieved from sources like [Landatlas](https://www.landatlas.de "Landatlas") or Wikipedia. Up until now, we analysed 54 such structural factors.** In further steps, we hope to gain insights on which behavior of decision makers and people living and working in the districts accelerates or slows the spread of the virus. We expect that over the course of the crisis and its aftermath, more data will become available that allows us to quantify and investigate critical behaviour. 

## 2. Clustering: Controlling Structural Variables to Identify Positive Deviance
**One important part of our analysis is the clustering of districts according to similarities in their structural factors.** This allows us to look deeper into how the Coronavirus is spreading across districts and make meaningful comparisons between districts with similar features. In other terms, we avoid comparing apples to oranges. We consistently find differences between rural areas and cities. We see that structural factors among cities vary more than among rural areas. This indicates that dividing into cities and rural areas would be a helpful next step. As clustering methods, we use Hierarchical Clustering, Principal Component Analysis (PCA) and Uniform Manifold Approximation and Prediction (UMAP).
**Clustering is a first and crucial step to be able to identify positive deviants: Statistically controlling structural variables allows us to identify those counties and municipalities that outperform their “peers” although they are in the same cluster, thus have comparable structural conditions.**



