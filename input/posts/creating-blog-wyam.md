Title: Creating a blog with Wyam
Published: 2019/07/07
Tags: 
    - blogging
    - wyam
---
A common piece of advice I see on Twitter from people in the industry with blogs is to write the posts for yourself as an archive of what you've done. So what better place to start than this blog?

I've attempted to start a blog several times over the years at this point. It never seems to get out the door, whether it's making sure the design is correct, the performance as fast as possible, the CI/CD pipelines are setup or that SSL is correctly configured. Still, it never gets out the door. Having read [ReWork](https://basecamp.com/books/rework) lately I decided to treat my blog like an MVP (minimum viable product), getting something out the door and refining it later. 

## Why Wyam

I have a few key considerations when it comes to creating a blog:

* I want it to be fast
* Creating a new post should be simple
* I don't want to write the entire structure myself (blogs are largely a solved problem) but I want to be in control
* I want it to be in a language I've worked with before (less cognitive load)
* I don't want to use a platform that gates posts
* I want to host it for free
* I want the deployment to be simple

The fastest you can get with code is to do nothing. A static site means our page is just an asset to serve, no back-end controllers performing logic to decide the page content or render it out. There are many static site generators and a lot of them have options for creating a blog. After some consideration I chose [Wyam](https://wyam.io/). There are a number of reasons for this:

* It's written in C# and is using .Net Core. I'm fairly comfortable with C# and have been wanting to look more at .Net Core. Wyam pipelines may be a good avenue into it
* RSS and Atom feeds out of the box
* Fast to get going, I was up and running in a couple of minutes
* Some simple themes that are easy to customise
* Posts are just Markdown files
* OSS on GitHub

Within a few minutes of installing the Wyam CLI tool, following the usage instructions and making some configuration changes to personalise the blog to myself, I had a site up and running locally. I just needed somewhere to host it.

## Hosting on Netlify

I attended a local dev group evening a number of months back and one of the talks was given by a dev advocate for [Netlify](https://www.netlify.com/). Netlify is, at it's a core, a static site host. It takes care of deployment and includes the ability to use a custom domain and automatically provision a Let's Encrypt certificate for it. They provide preview sites for every deploy that's done and any deploy can be chosen to be published as the live version, taking effect in only a few seconds. Deployments can be achieved by pointing at a GitHub repo and allowing webhooks to post whenever commits are pushed. Best of all, it's free for my purposes (I didn't realise until later but the Wyam site is hosted on Netlify). I've found using Netlify to be fast and intuitive and it suits my needs for the present time.

## Putting it together

Having constantly spent a lot of time on scrapped blogs, I found that within a couple of hours of sticking to the MVP strategy I had my blog choices made and had deployed it. Sure it's still using one of the out of the box themes but it's clean and readable which is good enough for an MVP. I can tweak the design going forward to suit my tastes and in the meantime, I'll still have a blog on the internet instead of languishing forever in a repo. Focusing on blogging for myself as an archive also removed the pressure of finding something novel and insightful to write about. Hopefully, this brief overview of the choices I made provides something useful to someone else who stumbles across it.