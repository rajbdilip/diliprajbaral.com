---
layout: default
title: Home
---
Hi, I'm Dilip. I write about software engineering - what I build, what breaks, and what I learn.

## Recent posts
<ul>
{% for post in site.posts limit:5 %}
<li>
  <a href="{{ post.url }}">{{ post.title }}</a>
  <small> - {{ post.date | date: "%b %-d, %Y" }}</small>
</li>
{% endfor %}
</ul>
