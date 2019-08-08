---
layout: archive
permalink: /application/
title: "海外大学院出願ー虎の巻"
author_profile : true
header:
  image: "/images/IMGP0327.JPG"
---

{% include base_path %}
{% include group-by-array collection=site.posts field="tags" %}

{% for tag in group_names %}
  {% assign posts = group_items[forloop.index0] %}
  <h2 id="{{ tag | slugify }}" class="archive__subtitle">{{ tag }}</h2>
  {% for post in posts %}
    {% include archive-single.html %}
  {% endfor %}
{% endfor %}
