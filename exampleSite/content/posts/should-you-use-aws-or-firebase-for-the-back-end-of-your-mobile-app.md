---
title: Should You Use AWS or Firebase For the Back end of Your Mobile App?
date: 2020-08-23T17:50:30.621Z
tags:
  - firebase, aws,
categories:
  - hosting
description: "One Is Not Better Than the Other One Why? Because the right
  question to ask is: “Which is the right solution for your requirements?”  I
  have been developing native Android apps for quite a while and have recently
  started developing mobile applications in Flutter and I have used both
  Firebase and AWS as back-end services.  But I recently had to find a solution
  for a mobile app and actually spent a lot of my time deciding between the
  right service for the back end."
featured_image: /images/1_a0bdxhaicfheazb1jbinra.png
---
<!--StartFragment-->

![Image for post]()

We are going to compare these two services in the following order:

1. What do they have in common?
2. How to integrate them with your front end?
3. Their strengths.
4. Their pricing.
5. Efforts required to build and maintain.
6. Final thoughts.

Alright, before we get started, I just want to clear something up before any of the die-hard fans of either of these services get upset with me…

- - -

# One Is Not Better Than the Other One

## Why?

Because the right question to ask is: “Which is the right solution for your requirements?”

I have been developing native Android apps for quite a while and have recently started developing mobile applications in [Flutter](https://flutter.dev/) and I have used both Firebase and AWS as back-end services.

But I recently had to find a solution for a mobile app and actually spent a lot of my time deciding between the right service for the back end.

So, here I am sharing my insights and understanding with you to maybe help you choose the right service without wasting much time.

- - -

# What Do These Services Have in Common?

Core features like:

* Auth
* Push notifications
* Storage
* Hosting
* Analytics

These are all offered so that you can easily deploy your serverless solution using any of these platforms.

- - -

# How Do You Want to Integrate Your Back End With Your App?

The most popular way of integrating these services is by using their SDKs but does that fit your requirements?

![Image for post](https://miro.medium.com/max/60/0*JigVAG74p3GpS9Wy?q=20)

![Image for post](https://miro.medium.com/max/7673/0*JigVAG74p3GpS9Wy)

Photo by [Will Porada](https://unsplash.com/@will0629?utm_source=medium&utm_medium=referral) on [Unsplash](https://unsplash.com/?utm_source=medium&utm_medium=referral)

## Firebase

Firebase provides an SDK for Android, iOS, and the web so you, being the front-end dev, can actually build a data-driven application easily without having to depend on back-end skills.

Firebase also has a REST API which you can use in case you want to build a custom API of your own (as per your requirements).

## AWS

AWS provides a very nice solution for mobile devs called [AppSync](https://aws.amazon.com/appsync/) which you can use for integrating into your Android, iOS, and React Native.

There is no official support for Flutter in AWS AppSync, yet, as you can read on [this website](https://github.com/aws-amplify/amplify-js/issues/1852).

You will have to create an API of your own if you want to use Flutter for the front end.

## Suggestions

* Seeing the complexity and business requirement of your solution, and keeping scalability in mind, decide whether you need to create an API or not.
* If you are going with having an API, then the dependency on SDKs goes away. Plus having an API makes a lot more sense for bigger projects.
* If your solution is simple, and you don’t want to invest in having an API then choose the service/front-end framework that provides SDKs so as to directly integrate your back end into your front end.

- - -

# Let’s See Their Strengths

Both Firebase and AWS have their strengths, let’s see which one might serve you better?

![Image for post](https://miro.medium.com/max/60/0*NGeQwMWv-DpxBZSE?q=20)

![Image for post](https://miro.medium.com/max/7500/0*NGeQwMWv-DpxBZSE)

Photo by [Vlad Hilitanu](https://unsplash.com/@vladhilitanu?utm_source=medium&utm_medium=referral) on [Unsplash](https://unsplash.com/?utm_source=medium&utm_medium=referral)

## AWS

**1. Set up different environments**

Different environments for development, testing, and production are more elegant in AWS.

Heck, you can do that in Firebase as well but you will have to set up different projects and it takes a bit more time to do so.

**2. Continuous deployment**

If you have used services like [Netlify](https://www.netlify.com/), AWS offers another elegant solution for continuous deployment. Again, you can do CD with Google Cloud as well but it requires a bit more configuration.

**3. GraphQL**

The AWS Amplify SDK for mobile application is closely integrated with [GraphQL](https://graphql.org/) and [Apollo](https://github.com/apollographql).

**4. Choice of database**

You have full control over what type of database you want to use in the back end. Firebase only offers NoSQL databases.

**5. Single packaged solution**

AWS offers all the services that your application might need. Hence, AWS is the single cloud solution you can completely rely on to back you up with all your requirements.

If your whole back end is in one place, it’s easier to understand and maintain.

## Firebase

**1. Dedicated database**

Firebase offers two dedicated database services, Cloud Firestore and Realtime Database.

Both of these databases are NoSQL databases so you don’t have to worry much about setting up databases and writing queries to deploy your data-driven app.

As long as your needs and requirements are simple and you know it won’t get a lot more complex in the future, then you can go with a NoSQL database.

**2. Callable functions**

Thanks to Firebase Cloud Functions, you can create Cloud Functions and set up triggers through a URL to write listeners to the database.

These functions are similar to AWS Lambda, but triggering a Lambda from an app requires you to set up an API gateway and add authorization logic which makes it a bit tougher.

**3. Quality control services**

Firebase offers a lot of services to monitor and maintain the quality of your application. Some of these services are:

* Dynamic links: To send users to the right place in your app whether or not it is already installed.
* Remote config: Customize and experiment with app behavior using a server-side configuration.
* Test lab: Test your apps across devices.
* In-app messaging: Sending campaigns for user engagement.
* Analytics: To help you plan your strategy for future releases and user engagement.
* ML Kit: To add the power of machine learning to your solution on the front end or the back end of your app.

- - -

# Platform Pricing (AWS vs. Firebase)

Both platforms have attractive pricing and even come with a free tier so that you don’t have to pay for anything unless you have a decent number of active users.

![Image for post](https://miro.medium.com/max/60/0*MEoxMoUxwp2GWsXy?q=20)

![Image for post](https://miro.medium.com/max/4793/0*MEoxMoUxwp2GWsXy)

Photo by [Hello I’m Nik 🍌](https://unsplash.com/@helloimnik?utm_source=medium&utm_medium=referral) on [Unsplash](https://unsplash.com/?utm_source=medium&utm_medium=referral)

## AWS

AWS mastered pricing for its services and offers many great services for prices that are a lot cheaper. They have actually been able to reduce the pricing of their services over time by over 80%.

This is the reason you will find AWS to be a bit cheaper than GCP for most of the services.

For building real-time applications, AWS offers [DynamoDB](https://aws.amazon.com/dynamodb/) which is comparatively expensive.

For Cloud Functions, AWS offers services at half the price compared to Firebase Cloud Functions.

## 2. Firebase

Whereas AWS is cheaper for some services, Firebaseoffers a few completely free services like:

1. User Authentication — With [FirebaseAuth](https://firebase.google.com/docs/reference/android/com/google/firebase/auth/FirebaseAuth) which is equivalent to [AWS Cognito](https://aws.amazon.com/cognito/).
2. Push Notifications — With Firebase Cloud Messaging which is equivalent to the Simple Notification Service in AWS.

For building real-time applications, Firebase seems a lot cheaper and easier to set up compared to AWS. Firebase takes care of its real-time syncing of data without you having to worry much about it.

As the number of users scales up, Firebase clearly seems like a better choice for building realtime applications.

But if you are not careful enough with your query optimizations, Firebase will send you a $30000 bill.

## [How NOT to get a $30k bill from Firebase](https://medium.com/@PurpleGreenLemon/how-not-to-get-a-30k-bill-from-firebase-37a6cb3abaca)

### [the secret is in the architecture](https://medium.com/@PurpleGreenLemon/how-not-to-get-a-30k-bill-from-firebase-37a6cb3abaca)

#### [medium.com](https://medium.com/@PurpleGreenLemon/how-not-to-get-a-30k-bill-from-firebase-37a6cb3abaca)

BTW, Google has let go of a few cases after understanding what happened. Thank you, Google.

There is something that costs more than platform pricing…

- - -

# Time and Labor

Yup, this is an important factor to consider because you will be dependent on resources to set up, build, and maintain your app architecture.

![Image for post](https://miro.medium.com/max/60/0*CP3f70ZwRUYTXO8A?q=20)

![Image for post](https://miro.medium.com/max/7500/0*CP3f70ZwRUYTXO8A)

Photo by [Omar Albeik](https://unsplash.com/@omaralbeik?utm_source=medium&utm_medium=referral) on [Unsplash](https://unsplash.com/?utm_source=medium&utm_medium=referral)

## Firebase

Firebase is really simplified and very straightforward to use. The front-end devs can actually create and maintain the whole back end all on their own with a little knowledge about setting things up.

For creating real-time applications, Firebase takes care of a lot of the complexity and gives you a very powerful and simple-to-use SDK, saving you a lot of time and time is money.

## AWS

Since AWS offers ten times the services Firebase offers, it gets ten times more complex to use and maintain as well. All I am trying to say is that there is a bit of a learning curve to AWS as compared to Firebase.

For creating real-time applications, you will want to use the GraphQL API along with a DynamoDB instance which again is a NoSQL database, but you will have to set up the API and the database which may seem like overkill for a simple real-time application.

- - -

# Final Thoughts

![Image for post](https://miro.medium.com/max/60/0*EG-_V52phphmvWx9?q=20)

Photo by [James Pond](https://unsplash.com/@jamesponddotco?utm_source=medium&utm_medium=referral) on [Unsplash](https://unsplash.com/?utm_source=medium&utm_medium=referral)

## Firebase

* Easy to set up, use, and maintain.
* Requires you to make fewer decisions, a great fit for simple applications.

## AWS

* More flexibility on offer, which helps a lot in building large, complex applications, but might be overkill for simple applications.
* A potential solution for all your application needs, you can build a neatly packaged solution but it might cost a bit more.

There you go! I hope this helps you make the right decisions and ask better questions when you are trying to architect your application.

Republished from : <https://medium.com/better-programming/should-you-use-aws-or-firebase-for-the-back-end-of-your-mobile-app-a28f93540520>

<!--EndFragment-->