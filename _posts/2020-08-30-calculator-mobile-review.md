---
title: "Cal-culator project refactoring to mobile!"
date: 2020-08-30 23:05:50
categories: jekyll update
---

It's been 6 weeks since I've worked with my first proejct with codestates - cal-culator.It is a web application that calculates user's daily intake and summarize / visualize the data. They will be able to get
- total daily intake (and how much nutrients they've consumed)
- weekly, monthly calorie statistics

I thought it was a great idea to work on this project again, only this time, transfer it to a mobile platform. However, There are some libraries that me and my teammate wanted to try: MongoDB and GraphQL. I've heard about these two libraries so much, but never had the chance to use them at all.

Some of the great stuff about MongoDB are...
- have very flexible document schemas
- easy to set up, easy to learn and use
- changing structure of the "Columns" are easy

Yes, the benefits of RDBMS like MySQL may dominate MongoDB when the size of the app gets big, but for small side projects(like this), I would probably go for MongoDB.

Some of the great stuff about GraphQL are...
- they act like a graph - interwining all sorts of fileds and records
- created by Facebook (which means, you know, constant fix and updates on cool new features)
- can fetch ONLY the data of choice (disregard all unnecessary ones)

However, GraphQL do have some disadvantages as well. All queries made through GraphQL will always return HTTP status of 200(even with the wrong queries). So, you do need to carefully process the errors, or just make it right when you design the schema and all.

So far, the basic structure (and structure only, no functionality implemented yet) of client is set up, and graphql / mongoDB interactions are all set up as well. All that is left to this project now is
- implementing normal RESTful API methods when fetching data from spoonacular API (where we get our food data)
- setting up graphql functionality on the client side and making it interact with our server correctly.

As of now, I have no idea how to send bulk, repetitive data (case: when user decides to add several items to the database at once) via graphQL variables. I will write another article regarding this issue later on!

