---
layout: page
permalink: /publications/
title: publications
description: authors are listed in alphabetical order, which is the norm in theoretical computer science and mathematics.
years: [2024, 2023, 2022, 2021, 2020]
display_categories: [preprints, conference, thesis]
nav: true
nav_order: 1
---
<!-- _pages/publications.md -->
<div class="publications">

{% for category in page.display_categories %}
  <h2 class="category">{{category}}</h2>
  {% for y in page.years %}
    {% bibliography -f {{ site.scholar.bibliography }} -q @*[dcat={{category}} && year={{y}}]* %}
  {% endfor %}
{% endfor %}



</div>
