---
layout: single
title: Home
---
Hi, I'm Dilip. I write about software engineering - what I build, what breaks, and what I learn.

## Recent posts
{% for post in site.posts limit:5 %}
{% assign teaser = post.header.teaser | default: post.header.image %}
<article class="archive__item">
  {% if teaser %}
  <div class="archive__item-teaser">
    <img src="{{ teaser | relative_url }}" alt="">
  </div>
  {% endif %}
  <div class="archive__item-body">
    <h3 class="archive__item-title"><a href="{{ post.url }}">{{ post.title }}</a></h3>
    <p class="archive__item-excerpt">{{ post.excerpt | strip_html | truncate: 160 }}</p>
  </div>
</article>
{% endfor %}
