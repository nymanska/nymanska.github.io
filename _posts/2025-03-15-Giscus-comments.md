---
title: "Adding Comments Section to Jekyll Site with Giscus"
#description: How to add comment section to Jekyll page and why I chose Giscue.
date: 2025-03-15 10:25:00 0100
categories: [Github]
tags: [code, github]  #TAG names should always be lowercase separated by comma
mermaid: false
image: 
  path: /assets/img/2025/Giscus-comments/cover.png
  lqtip: 
---


## Introduction
One of the reasons for [starting this blog](https://www.nymanska.com/posts/Welcome-blog/) is to have a space where I can share my thoughts, ideas, and insights from both my professional and private life. Posting my thoughts publicly on this platform is a great way to express myself, but another key reason is to connect and interact with like-minded people. One way of doing that is by adding a way for readers to comment on my articles.

This website is built on [Jekyll](https://jekyllrb.com/) using the [Chirpy theme](https://github.com/cotes2020/jekyll-theme-chirpy), and there are many ways to add a commenting system to a Jekyll site. In this article, I’ll go through why I chose Giscus, the steps to get it up and running, and how to customize it to fit your site.

## Why I Chose Giscus for my comments feature
There are several ways to add comment functionality to a Jekyll site. Some of the main alternatives are **Disqus**, **Staticman**, and **Giscus**.

**[Disqus](https://disqus.com/)** seems like the most straightforward option, offering an easy setup and a simple way for viewers to log in or create an account to leave comments. However, I wasn’t comfortable with the privacy aspects of using Disqus, and I also wanted to avoid relying on third-party services.

**[Staticman](https://staticman.net/)** was another interesting option, but after some research, I found that the repository hasn’t been actively maintained in a few years. Because of this, I was hesitant to invest time in figuring out whether it would still work reliably.

**[Giscus](https://github.com/giscus/giscus)**, however, caught my eye as a really nice alternative. It can be customized to fit with emoji interactions and offers great overall customization options. One of the main drawbacks, in my opinion, is that it requires a GitHub account. I knew that only a small percentage of my blog readers would actually use a GitHub account, but I decided to go with Giscus anyway. The simplicity of setting it up was appealing, and I wanted to give it a try. 

**The pros and cons I see are:**
- 👍 Open source
- 👍 Reduce spam
- 👍 Privacy-friendly
- 👍 Visual Customizable
- 👍 Emoji interaction feature
- 👎 Require a GitHub account

## What is Giscus
Giscus is a a comments system powered by [GitHub Discussions](https://docs.github.com/en/discussions). Let visitors leave comments and reactions on your website via GitHub - That's it!

A few articles that helped inspire my choice of Giscus 💡
* [Yury Zhauniarovich](https://zhauniarovich.com/post/2021/2021-06-giscus/)
* [Thiago Alves](https://thiagoalves.ai/adding-comments-to-jekyll-using-giscus/)
* [Martin's Tech Journal](https://blog.martinp7r.com/posts/adding-giscus-comments-to-my-blog/)

## How to set-up

### Step 1: Create a new Github repository for storing comments
![Adding giscus comments to jekyll site](/assets/img/2025/Giscus-comments/giscus-new-repo.png)

### Step 2: Enable Discussions feature in repository settings
![Adding giscus comments to jekyll site](/assets/img/2025/Giscus-comments/giscus-enable-discussions.png)

### Step 3: Install Giscus App at your new repository
1. Head over to Github marketplace: https://github.com/marketplace/giscus
2. Click the Install it for Free button in the bottom of the page
3. Review the "Free" order, add billing information and click the Save billing information
4. Click Complete order and begin installation button
5. Select the repository where you want to store the comments (see Step 1), and click Install.
6. Done!

### Step 4: Enable Giscus Comments in your website repository
1. Head over to Giscus App https://giscus.app to create a customization script which will be used in your website's page
2. Add the repository name (for me this was: nymanska/nymanska.github.io-Comments)
![Adding giscus comments to jekyll site](/assets/img/2025/Giscus-comments/Giscus-setup-add-repo.png)
3. Add customization features you would like for your website such as placement of comment box, color theme, enable reactions, and more.
4. The Giscus.app page will automatially create your giscus script. Mine looks as below:

```
<script src="https://giscus.app/client.js"
        data-repo="nymanska/nymanska.github.io-Comments"
        data-repo-id="R_kgDOOI8GbQ"
        data-category="General"
        data-category-id="DIC_kwDOOI8Gbc4CoDnd"
        data-mapping="pathname"
        data-strict="0"
        data-reactions-enabled="1"
        data-emit-metadata="0"
        data-input-position="top"
        data-theme="preferred_color_scheme"
        data-lang="en"
        crossorigin="anonymous"
        async>
</script>
```

5. Add the Giscus script to your website / blog
My site is built with the Chirpy Theme which fortunately already has built-in support for Giscus comments defined in the _config.yml file (if you are using a different theme you might want to add the script in either your config, post or other file.) Add the Giscus script information in the _config.yml file_
![Adding giscus comments to jekyll site](/assets/img/2025/Giscus-comments/giscus-new-repo.png)

6. Add the Script from Step 4 in the bottom of each blog post.
There might be a better way of doing this without having to post the scrip in every blog post but I haven't found out how to make that work yet.

### Step 5. Try it out!
![Adding giscus comments to jekyll site](/assets/img/2025/Giscus-comments/new-comment.png)

## Final Words
After researching different options for adding comment functionality to my blog, I decided that **Giscus** was the right choice for me, and I’m looking forward to trying it out over the next couple of months.

Are you using a different comment system for your Jekyll site? I’d love to hear about your experiences with other solutions or if this article was helpful for you.

Feel free to share your thoughts - and if you want to test out my new comment section, go ahead and leave a comment below! 👇



<script src="https://giscus.app/client.js"
        data-repo="nymanska/nymanska.github.io-Comments"
        data-repo-id="R_kgDOOI8GbQ"
        data-category="General"
        data-category-id="DIC_kwDOOI8Gbc4CoDnd"
        data-mapping="pathname"
        data-strict="0"
        data-reactions-enabled="1"
        data-emit-metadata="0"
        data-input-position="top"
        data-theme="preferred_color_scheme"
        data-lang="en"
        crossorigin="anonymous"
        async>
</script>
