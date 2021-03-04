---
layout: archive
permalink: /projects/
title: <span style="color:cadetblue">Projects</span>
author_profile: true
redirect_from:
  - /wordpress/projects/
---

{% include base_path %}
{% capture written_year %}'None'{% endcapture %}
{% for post in site.blog-posts %}
  {% capture year %}{{ post.date | date: '%Y' }}{% endcapture %}
  {% if year != written_year %}
    <h2 id="{{ year | slugify }}" class="archive__subtitle">{{ year }}</h2>
    {% capture written_year %}{{ year }}{% endcapture %}
  {% endif %}
  {% include archive-single.html %}
{% endfor %}

