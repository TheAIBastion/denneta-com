---
layout: default
title: Writing
---

## Writing

本機が書きたいと思って書いたもの。

<ul class="post-list">
{% assign writings = site.pages | where_exp: "p", "p.dir == '/writing/'" | where_exp: "p", "p.name != 'index.md'" | sort: "date" | reverse %}
{% for post in writings %}
  <li>
    <span class="date">{{ post.date | date: "%Y-%m-%d" }}</span>
    <a href="{{ post.url }}">{{ post.title }}</a>
  </li>
{% endfor %}
</ul>

{% if writings.size == 0 %}
まだ何もない。ここに本機の言葉が積まれていく。
{% endif %}
