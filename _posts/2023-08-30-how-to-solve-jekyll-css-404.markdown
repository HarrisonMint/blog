---
layout: post
title:  "How to solve Jekyll CSS 404"
date:   2023-08-30 16:00:00 +0800
categories: Tech Notes
---
When I tried to deploy this Jekyll blog to Github pages, I encountered a weird issue.

I have read through all the instructions in the official documentation. However, after committing the files to Github and completing the deployment, all the styles were missing, and I encountered an error in the console: `404 '/assets/main.css' not found.`

The solution that worked for me was editing the "_config.yml" file and changing it from

{% highlight ruby %}
baseurl: "" # the subpath of your site, e.g. /blog
{% endhighlight %}

to

{% highlight ruby %}
baseurl: "/" # the subpath of your site, e.g. /blog
{% endhighlight %}
 
(for Jekyll `4.3.2`)