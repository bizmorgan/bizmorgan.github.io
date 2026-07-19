---
layout: page
title: "Blog"
---

This is where I will publish blog posts and longer updates.

{% assign blog_pages = site.pages | where_exp: "item", "item.path contains 'blog/' and item.name != 'index.md'" %}

{% if blog_pages.size > 0 %}
  {% for item in blog_pages %}
    <p><a href="{{ site.github.url }}{{ item.url }}">{{ item.title | default: item.name }}</a></p>
  {% endfor %}
{% else %}
  <p>No blog posts have been added yet.</p>
{% endif %}