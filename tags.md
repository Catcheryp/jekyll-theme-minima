---
layout: page
title: Tags
permalink: /tags/
---

{% assign ordered_tags = site.tags  %}
<div class="tag-list">
{% for tag in ordered_tags %}
    <a href="#{{ tag[0] }}" class="post-tag">{{ tag[0] }}</a>
{% endfor %}
</div>

{% for tag in ordered_tags %}
  <h2 id="{{ tag[0] }}">{{ tag[0] }} <small>[{{ tag[1].size }}]</small></h2>
  <ul>
    {% for post in tag[1] %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}