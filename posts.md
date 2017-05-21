---
layout: page
title: Posts
permalink: /dev-blog/posts
---
<div>
<ul>
{% assign posts_list = site.posts %}
    {% for node in posts_list %}
      {% if node.title != null %}
        {% if node.layout == "post" %}
          <li><a href="{{ node.url }}">{{ node.title }}</a> ({{ node.date }})</li>
        {% endif %}
      {% endif %}
    {% endfor %}
</ul>
</div>