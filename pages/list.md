---
layout: default
title: Blog Posts List
permalink: /posts/
---

-----------------------------------
{% for category in site.categories %}

  <uli>
    <section class="text-center">
      <div class="container">
          <div class="col-lg-8 col-lg-offset-2">
              <h3> {{ category | first }} </h3>
              {% for posts in category %}
                  {% for post in posts %}
                    {% if post.title != null || post.link != null %}
                      <ul style="list-style: none;padding-left: 0;">
                        <a title="Published at {{ post.date }}" href="{{ post.link }}" class="btn btn-default btn-lg"> {{ post.title }}</a>
                      </ul>
                    {% endif %}
                  {% endfor %}
              {% endfor %}
          </div>
      </div>
    </section>
  </uli>
  ----------------------------------

{% endfor %}
