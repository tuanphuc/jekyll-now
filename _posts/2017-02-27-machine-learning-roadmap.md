---
layout: post
title: Machine Learning roadmap for engineers
---

Before going into details of a Machine Learning (ML) roadmap, I want to clarify that I am an embedded engineer who are amazed by the beauty of ML and have started learning it for just over a year. So everything I write in this blog is subjective to my point of view. 

ML is a very interesting field to study. There is a fast growing need of engineers who had a computer science degree and want to step in this field and I am an example. However, it is not easy to have a clear study plan so that you can actually understand the background of ML and then eventually become a ML engineer.

Although there are a lot of instructions, suggestions and even detailed roadmaps out there but I can't even know where to start because of the redundance of information in those approches. One of the most popular machine learning roadmap is one on github:

[https://github.com/ZuzooVn/machine-learning-for-software-engineers](https://github.com/ZuzooVn/machine-learning-for-software-engineers)

which proposes a lot of studying resources which are highly recommended by many people in the field. But I found hard to start when I look at a long list of resources which lacks of subtantial details in plan needed to be in a true roadmap. In this blog I will share with you a roadmap that I think concrete to learn ML based on my own experiences so it's up to you to decide to follow.

##1. Theory

In my opinion, if you understanding theoritically a problem, you can learn much faster afterward. So first, you need to build your basic theory backgound of statistical learning (foundation of ML). Two books that are highly recommended is:

  - An Introduction to Statistical Learning with Applications in R of Gareth James, Daniela Witten, Trevor Hastie, and Robert Tibshirani
  -  The Elements of Statistical Learning: Data Mining, Inference, and Prediction of Trevor Hastie, Robert Tibshirani, and Jerome Friedman
  
Those books are 2 textbook used in the course [CS 189/289A Introduction to Machine Learning](https://people.eecs.berkeley.edu/~jrs/189s16/). They are available to download and you can follow the schedule of lectures to have a plan of reading those two books. There are also homeworks and lecture videos on youtube that are very useful. The first book introduces basic definition and popular methods, algorithms in Statistical Learning that are very accessible to beginers who are not specilised in statistic. The latter book covers all those things but in a higher level with detailed explanations and formulas that give you a great insight into what is behind all the different methods.

##2. Practices

> What I cannot create, I do not understand - Richard Feynman

The next step is to implement some or all of the algorithms in the books to fully understand how they work. You can also learn a lot of programming techniques required to implement efficiently those algorithms because the scale of ML. Practically you are equipped all the things you need to implement ML algorithms. I found a repository on github that has those algorithms implemented from scratch which I found very useful:

[https://github.com/eriklindernoren/ML-From-Scratch](https://github.com/eriklindernoren/ML-From-Scratch)

From this point onward you have solid theoretical and practical background to develop your own ML projects. If you use libraries like tensorflow, keras or Pytorch, it's much easier to understand how models are created in those libraries and more importantly you understand clearly how every parameter in those models reflects on the final result.

##3. Competitioins (optional)

If you want to improve your skills in ML by competing, [kaggle.com](kaggle.com) is a pretty good place to start. One of the advantages of competting on kaggle is that you can build a profile as you compete. And that profile can play an important role in your career.

I will end this blog with a suggestion on another book that is helpful too:

[Patern recognition and Machine learning by Christopher M. Bishop](http://users.isr.ist.utl.pt/~wurmd/Livros/school/Bishop%20-%20Pattern%20Recognition%20And%20Machine%20Learning%20-%20Springer%20%202006.pdf)

This books with 2 other books introduced above can be used together. I might add more infos to this roadmap and extend this blog with some ideas on learning Deep Learning so if you find this post interesting, pin it. I'm happy to get your feedback to make this roadmap more concrete so don't hesitate to email me to: [phan@tuanphuc.com](mailto:phan@tuanphuc.com). 

Hope that this roadmap can help you.
