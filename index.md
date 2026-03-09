---
layout: default
title: People
permalink: /
---

<ul class="post-list">
{% for post in site.categories.people %}
  <li>
    <a href="{{ post.url | relative_url }}">
      <span class="title">{{ post.title }}</span><time>{{ post.date | date: "%Y" }}</time>
    </a>
  </li>
{% endfor %}
</ul>

{% for post in site.categories.people %}
<div class="arc-post-content" id="arc-content-people-{{ forloop.index }}" style="display:none;">
  <h2>{{ post.title }}</h2>
  {{ post.content }}
</div>
{% endfor %}

<div class="arc-scroll">
  <div class="arc-content-area" id="arc-content-area"></div>
  <div class="arc-items">
    {% for post in site.categories.people %}
    <div class="arc-item" data-index="{{ forloop.index0 }}" data-content-id="arc-content-people-{{ forloop.index }}" data-href="{{ post.url | relative_url }}">
      {{ post.short_title | default: post.title }}
    </div>
    {% endfor %}
  </div>
</div>
