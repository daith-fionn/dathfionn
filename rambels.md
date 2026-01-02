---
layout: default
title: rambels
permalink: /rambels/
---

<ul class="post-list">
{% for post in site.categories.rambels %}
  <li>
    <a href="{{ post.url | relative_url }}">
      <span class="title">{{ post.title }}</span><time>{{ post.date | date: "%Y" }}</time>
    </a>
  </li>
{% endfor %}
</ul>
