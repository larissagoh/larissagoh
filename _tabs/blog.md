---
title: Blogs
icon: list-ul
order: 2
---

{% assign blog_posts = site.posts | where_exp: "post", "post.categories contains 'blog'" %}

{% for post in blog_posts %}
- [{{ post.title }}]({{ post.url }}) — {{ post.date | date: "%Y-%m-%d" }}
{% endfor %}
