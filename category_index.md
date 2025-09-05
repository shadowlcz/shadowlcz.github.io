---
layout: page
title: "Posts by Category"
permalink: /categories/
---

<ul>
{% for category in site.categories %}
  <li>
    <a href="#{{ category[0] }}">{{ category[0] }} ({{ category[1].size }})</a>
  </li>
{% endfor %}
</ul>

{% for category in site.categories %}
  <h2 id="{{ category[0] }}">{{ category[0] }}</h2>
  <ul>
    {% for post in category[1] %}
      <li><a href="{{ post.url }}">{{ post.title }}</a> <small>{{ post.date | date: "%Y-%m-%d" }}</small></li>
    {% endfor %}
  </ul>
{% endfor %}