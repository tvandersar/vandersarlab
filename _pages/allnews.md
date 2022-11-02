---
title: "News"
layout: textlay
excerpt: "Allan Lab at Leiden University."
sitemap: false
permalink: /allnews.html
---

# News

{% for article in site.data.news %}
<b>{{ article.date }}</b>
{{ article.headline | markdownify}}
{% endfor %}
