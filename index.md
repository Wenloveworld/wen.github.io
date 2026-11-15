---
layout: page
title: 分类
permalink: /categories/
---

{% assign categories = site.categories | sort %}
{% for category in categories %}
  <h2>{{ category[0] | escape }}</h2>
  <ul>
    {% for post in category[1] %}
      <li><a href="{{ post.url | relative_url }}">{{ post.title | escape }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}
