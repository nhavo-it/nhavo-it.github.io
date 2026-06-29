---
layout: page
title: Bài viết
permalink: /blog
---

{% for post in site.posts %}
<article>
  <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
  <time>{{ post.date | date: "%d/%m/%Y" }}</time>
  {% if post.excerpt %}
    <p>{{ post.excerpt | strip_html | truncate: 150 }}</p>
  {% endif %}
</article>
{% endfor %}

{% if site.posts.size == 0 %}
  <p>Chưa có bài viết nào.</p>
{% endif %}
