---
layout: default
title: Project List
permalink: /pages/list/
---


{% for category in site.categories %}

  ------------------------------------------------------------------------------------------
  <li>
    <h1> {{ category | first }} </h1>
    <ul>
    {% for posts in category %}
      {% for post in posts %}
        <li><a href="{{ post.url }}">{{ post.title }}</a></li>
      {% endfor %}
    {% endfor %}
    </ul>

    <br/><br/>
  </li>
{% endfor %}
