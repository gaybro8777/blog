---
title: "All the Serverless announcements at re:Invent 2018"
description: "Not at AWS re:Invent? That's ok; we're compiling all the most important serverless announcements and updates. Updating live all week."
date: 2018-11-27
thumbnail: 'https://s3-us-west-2.amazonaws.com/assets.blog.serverless.com/reinvent/reinvent-updates-thumb.png'
heroImage: 'https://s3-us-west-2.amazonaws.com/assets.blog.serverless.com/reinvent/reinvent-updates-header1.gif'
category:
  - news
authors: 
  - AndreaPasswater
---

*Last updated: Nov 27, 8:49 AM*

re:Invent 2018 has begun! But there is ever so much to track.

If last year is any indication, we expect AWS to have a long list of serverless-centered announcements and launches. If you want to keep up, you've come to the right place.

We're watching all the keynotes and announcements live as they happen, and compiling the "what it is" and the "why it matters" right here. Updating live all week!

Oh, and while you're here, you should [check out our re:Invent virtual hackathon](https://serverless.com/blog/no-server-november-reinvent-hackathon). You can participate from anywhere, even if you're not at the conference, and win prizes while helping non-profits along the way.

#### re:Invent 2018 announcements

*Pending*

#### Pre-re:Invent announcements

* [Amplify Console](#amplify-console)
* [AWS open-sources Firecracker virtualization technology](#aws-open-sources-firecracker-virtualization-technology)
* [S3 Batch Operations (preview)](#s3-batch-operations-preview)
* [Serverless Aurora Data API](#serverless-aurora-data-api)
* [Preview of Aurora Serverless (PostgreSQL)](#preview-of-aurora-serverless-postgresql)
* [AppSync Pipeline Resolvers](#appsync-pipeline-resolvers)
* [Lambda + Kinesis Data Streams Upgrades](#lambda--kinesis-data-streams-upgrades)
* [Python 3.7 for Lambda](#python-37-for-lambda)

#### Announcements:

##### [Amplify Console](https://aws.amazon.com/about-aws/whats-new/2018/11/announcing-aws-amplify-console/)

**What it is:** Deployment and hosting platform for web applications with serverless backends. Easily build and deploy your static site using Gatsby, Hugo, Jekyll, or other static site generators, as well as your backend APIs.

**Why it matters:** JAMStack, here I come! This is a low-config way to manage your JAMStack. Think Netlify, but with backend functions as well. For many projects, this is a great way to get your code from dev to production quickly.

##### [AWS open-sources Firecracker virtualization technology](https://aws.amazon.com/blogs/aws/firecracker-lightweight-virtualization-for-serverless-computing/)

**What it is:** Firecracker is a virtual machine manager built by AWS that hosts Lambda functions and Fargate containers. It's extremely lightweight, able to create a microVM in as little as 125 milliseconds.

**Why it matters:** For most Serverless users, this isn't something you need to care about. Yes, #ServerlessHasServers, but you don't need to know about them! However, it's still really exciting to see the amazing tech that is underlying all of these services from AWS. Further, the fact that Firecracker is open source means that it could receive community contributions that continue to push the envelope on serverless performance. It's great to see AWS making core, original contributions to the open-source community.

##### [S3 Batch Operations (preview)](https://aws.amazon.com/about-aws/whats-new/2018/11/s3-batch-operations/)

**What it is:** Select batches of existing objects in S3 to run actions on -- add tags, copy to another bucket, or even send to Lambda functions.

**Why it matters:** This eliminates a ton of toil around operating on existing objects in S3. You would need to write a ton of custom logic to make sure you're hitting the right objects, handling errors, etc. Now you can easily manipulate a huge block of objects in a single go.

##### [Serverless Aurora Data API](https://aws.amazon.com/about-aws/whats-new/2018/11/aurora-serverless-data-api-beta/)

**What it is:** An HTTP endpoint for accessing your Serverless Aurora database.

**Why it matters:** This is a big deal. In our post last year on [why Serverless Aurora is the future of data](https://serverless.com/blog/serverless-aurora-future-of-data/), we noted that an HTTP-accessible relational database would be a huge step forward for the Serverless ecosystem. AWS is starting to deliver on this promise.

Friend-of-the-Framework and all-around awesome guy [Jeremy Daly](https://twitter.com/jeremy_daly) has done a great [review of the Serverless Aurora Data API](https://www.jeremydaly.com/aurora-serverless-data-api-a-first-look/). TL;DR: It's not quite ready for primetime. AWS often releases things early and rapidly improves them, so look for this to get a lot better in 2019.

##### [Preview of Aurora Serverless (PostgreSQL)](https://aws.amazon.com/about-aws/whats-new/2018/11/sign-up-for-the-preview-of-amazon-aurora-postgresql-serverless/)

**What it is:** A PostgreSQL-compatible version of the Aurora Serverless database is now available in preview.

**Why it matters:** We're very bullish on Serverless Aurora being an important tool in the Serverless ecosystem. The MySQL-compatible database was released earlier this year, and now the PostgreSQL version is getting closer. This is great news for Postgres fans.

##### [AppSync Pipeline Resolvers](https://aws.amazon.com/about-aws/whats-new/2018/11/aws-appsync-launches-pipeline-resolvers-delta-sync-aurora-serverless-support/)

**What it is:** Break up GraphQL resolvers into multiple steps when using AppSync.

**Why it matters:** [AppSync is a great way to build Serverless GraphQL applications](https://serverless.com/blog/building-chat-appliation-aws-appsync-serverless/), and this service continues to get more and more powerful. The pipeline resolvers are great for adding authorization to the front of your GraphQL api or for more complex flows. AppSync is definitely a service to watch in 2019.

##### [Lambda + Kinesis Data Streams Upgrades](https://aws.amazon.com/about-aws/whats-new/2018/11/aws-lambda-supports-kinesis-data-streams-enhanced-fan-out-and-http2/)

**What it is:** AWS Lambda can now use Kinesis Data Streams Enhanced Fan-Out, a faster implementation of consumers for [Amazon Kinesis](https://aws.amazon.com/kinesis/)

**Why it matters:** The Enhanced Fan-Out for Kinesis Data Streams greatly increases the performance of Kinesis Data Streams. You can read up to 2MB per second per shard on your Kinesis Data Stream. Further, you can have multiple, independent consumers with the Enhanced Fan-Out that helps you get around the limitations of previous Kinesis consumers.

This is a huge step forward for fans of stream-based processing with AWS Lambda.

#### [Python 3.7 for Lambda](https://aws.amazon.com/about-aws/whats-new/2018/11/aws-lambda-supports-python-37/)

**What it is:** AWS Lambda now supports the Python3.7 runtime.

**Why it matters:** You get all the latest Python features with your Lambdas! The most exciting addition to Python3.7 is likely [dataclasses](https://docs.python.org/3/library/dataclasses.html) -- a much simpler way to define classes.

**How do I use it:** You can use Python3.7 in the Serverless Framework by setting `runtime: python3.7`. The built-in `aws-python3` template will use Python3.7 in the [next release of the Framework](https://github.com/serverless/serverless/pull/5505).