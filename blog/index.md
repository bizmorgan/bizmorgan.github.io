---
layout: page
title: "Blog"
---

This is where I will publish blog posts and longer updates.

{% assign blog_pages = site.data.settings.blog %}

{% if blog_pages.size > 0 %}
  {% for item in blog_pages %}
    <p><a href="{{ site.github.url }}{{ item.url }}">{{ item.name }}</a></p>
  {% endfor %}
{% else %}
  <p>No blog posts have been added yet.</p>
{% endif %}