---
title: "Publications and preprints"
layout: archive
permalink: /papers/
author_profile: true
---

{% include group-by-array collection=site.posts field="categories" %}

{% for category in group_names %}
  {% assign posts = group_items[forloop.index0] %}
  <h2 id="{{ category | slugify }}" class="archive__subtitle">{{ category }}</h2>
  {% for post in posts %}
    {% include archive-single-publ.html %}
  {% endfor %}
{% endfor %}