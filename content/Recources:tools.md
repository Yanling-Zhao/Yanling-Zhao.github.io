---
title: "Resources/Tools"
draft: false
menu:
  main:
    Name: "Resources/Tools"
    weight: 300
---

In this page, I will document and share some useful self-learn recources and tools.


### 1. How to extract Twitter data from Twitter Academic API?
---

Twitter data is one of the most frequently used data in computational social science research. Currently, there are two major ways for researchers to access the twitter data: One is [Twitter APIs](https://developer.twitter.com/en/docs/twitter-api) (all levels); another one is commercial third party platforms such as [Brandwatch](https://www.brandwatch.com/), [Synthesio](https://www.synthesio.com/).

I had experience with both Twitter Academic API and third party platforms, and I list some Pros/Cons of both ways here.
            
Twitter Academic API: (Pros) free, flexible, and full-archive history data; (Cons) Requiring programming skills as you need to write the code for access and scrape.

Third party platforms: (Pros) More user friendly interface/dashboard, you do not have to use programming skills, time saving when collecting large-scale data from cross platforms as most of those third party platforms allow you to select multiple data sources with the same search query ; (Cons) Paid, downloading limits per day or per downloading action.

For more systematic and scientific assessment of those different tools, you could read this paper: [Chen, K., Duan, Z., & Yang, S. (2022). Twitter as research data: Tools, costs, skill sets, and lessons learned. Politics and the Life Sciences, 41(1), 114-130](https://www.cambridge.org/core/journals/politics-and-the-life-sciences/article/twitter-as-research-data/6B31D18C5E2F9B8F9C0301BFB05F1C27).

If you have programming background and skills, I highly suggest you to try with the Twitter Academic API! Check out the [official Twitter Academic API documentations and Tutorials](https://developer.twitter.com/en/use-cases/do-research/academic-research/resources). If you use R, there is one R package ["academictwitteR"](https://github.com/cjbarrie/academictwitteR) that could help you collect tweets from new v2 API endpoint for the Academic Research Product Track and also convert JSON files into dataframe in R. From my experience, this package is super simple and easily to use, all functions work well except for the resume_collection() and update_collection() two functions. When you collect large volume of data, it is normal that your search query will be interrupted at some points. If that is the case for you, and above two functions also can not work out, one of the solutions is to run a new round of collection with the same query to collect remain tweets, set the end tweets date and time from where the previous collection stopped (You could check the last collected tweets' date and time in the "data_xxx.json"file). Note 1:The collection is processed from the newest dates and time back to the older dates and times. Note 2: The current cap of Twitter Academic API is set to 10 millions per month, plan your time schedule when you need to collect more than  10 millions' data.

If you use Python, there are also many Python packages, search on google!

I used the twitter Academic API v2 endpoint with "academictwitteR" package to collect more than 10 millions' tweets around the 2020 U.S. Presidential Election misinformation for my master thesis (costing more than 1 weeks), I will upload the scrape R script along with the dataset to the github later(also will update here) after I finish this project!

Good luck with your data collection trip!

### 2. How to build up a personal website?
---
I started learning web design in [Dr. Lei Guo](https://www.leiguo.net/)'s EM757 “User-Producers 2.0: Developing Interactivity” class. Largely credited to this class's content, there are different ways to create a website: 1. HTML + CSS coding by hand; 2. WYSIWYG Web authoring tools such as Adobe Dreamweaver; 3. Content management systems (CMS) such as Wordpress, Blogger.com, Drupal, and Joomla. 

We used the Wordpress combined with CSS and HTML for the course project. Later, I started learning another way for website building: Hugo + Github, this is exactly the way I used for this persobal website building! 

Here are some Pros and Cons of "Hugo + Github" approach I summarized upon my own experience: (Pros) 1. Totally free! You can host your website on the github without paying any fee for the hosting sites or domain name. Of cource, if you are not satisfied with this type of "https://<Github UserName> .github.io." domain name, you can buy a domain name separately. 2. It is faster and easier for you to update contents on Website, as Hugo documentation stated "Hugo is a static HTML and CSS website generator written in Go. It is optimized for speed, ease of use, and configurability." So, if you are blog writing enthusiasts, or you have the need to update text contents on your website frequently, go with Hugo!
 (Cons) 1. More complicated than using Content management systems (CMS) such as Wordpress, Blogger.com, Drupal, and Joomla, as you need to know and write basic HTML, CSS codes; 2. You have to adapt to write the code or content in text editor and Markdown file; 3. There is access limitation of Github host site, therefore, if you assume your website will have large volume of visitors, you'd better to buy a commercial host site.
 
 If you are ready to use "Hugo + Github", check out those super useful tutorials:
 
[Hugo official documentations and sources](https://gohugo.io/)

[Hongtao Hao](https://hongtaoh.com/): [如何零基础免费搭建个人网站](https://hongtaoh.com/cn/2021/03/02/personal-website-tutorial/), [How to Deploy A Hugo Website Using GitHub Pages](https://hongtaoh.com/en/2021/04/05/hugo-deploy-github-actions/)

Good luck with your website building!
