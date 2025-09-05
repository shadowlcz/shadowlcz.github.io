---
layout: page
title: "Posts by Tag"
permalink: /tags/
---

<ul>
{% for tag in site.tags %}
  <li>
    <a href="#{{ tag[0] }}">{{ tag[0] }} ({{ tag[1].size }})</a>
  </li>
{% endfor %}
</ul>

{% for tag in site.tags %}
  <h2 id="{{ tag[0] }}">{{ tag[0] }}</h2>
  <ul>
    {% for post in tag[1] %}
      <li><a href="{{ post.url }}">{{ post.title }}</a> <small>{{ post.date | date: "%Y-%m-%d" }}</small></li>
    {% endfor %}
  </ul>
{% endfor %}