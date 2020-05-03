---
title: "Publications and preprints"
layout: archive
permalink: /papers/
sidebar:
  - title: "Title"
    image: "/images/remi.jpg"
    image_alt: "image"
    text: "Some text here."
  - title: "Another Title"
    text: "More text here.
---

{% include group-by-array collection=site.posts field="categories" %}

{% for category in group_names %}
  {% assign posts = group_items[forloop.index0] %}
  <h2 id="{{ category | slugify }}" class="archive__subtitle">{{ category }}</h2>
  {% for post in posts %}
    {% include archive-single.html %}
  {% endfor %}
{% endfor %}