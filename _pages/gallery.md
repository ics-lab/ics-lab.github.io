---
layout: page
title: Gallery
permalink: /gallery
nav: true
nav_order: 4
images:
    slider: true
description: Our members and memories
---

<swiper-container keyboard="true" navigation="true" pagination="true" pagination-clickable="true" pagination-dynamic-bullets="true" rewind="true" autoplay="true">
{% for image in site.static_files %}
    {% if image.path contains 'img/group' %}
        {% if image.extname == '.PNG' %}
            <swiper-slide>{% include figure.html loading="eager" path=image.path class="img-fluid rounded z-depth-1" %}</swiper-slide>
        {% endif %}
    {% endif %}
{% endfor %}
</swiper-container>
<hr>
