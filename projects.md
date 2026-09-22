---
layout: default
title: Projects
---

<h2>projects</h2>
<div class="sec-line"></div>

{% assign project_posts = site.categories.project %}
{% if project_posts.size > 0 %}
<ul class="post-list">
  {% for post in project_posts %}
  <li class="post-item">
    <a href="{{ post.url }}">{{ post.title }}</a>
    <div class="post-date">{{ post.date | date: "%b %d, %Y" }}</div>
    {% if post.summary %}<div class="post-summary">{{ post.summary }}</div>{% endif %}
    {% if post.tags %}
    <div class="tags">
      {% for tag in post.tags %}<span class="tag">{{ tag }}</span>{% endfor %}
    </div>
    {% endif %}
  </li>
  {% endfor %}
</ul>
{% else %}
<p class="empty">No projects yet.</p>
{% endif %}
