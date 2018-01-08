---
bg: "tag.jpg"
layout: page
permalink: /posts/rwd/
title: "posts"
crawlertitle: "RWD笔记"
summary: "Posts about rwd"

---

{% for post in site.posts limit: 10 %}
	{% if post.tags contains "note_rwd" %}
  <article class="index-page">
    <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
	<span class="date">{{ post.date | date: "%d-%m-%Y"  }}</span>
	
	
		{{ post.excerpt }}
  </article>
	{% endif %}
{% endfor %}