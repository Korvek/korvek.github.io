---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
title:  
---
<h1>Game Developer Portfolio</h1>

{% assign solo = site.projects | where: "category", "solo" %}
{% assign prototypes = site.projects | where: "category", "prototype" %}
{% assign others = site.projects | where_exp: "p", "p.category != 'solo'" | where_exp: "p", "p.category != 'prototype'" %}

{% if solo.size > 0 %}
<h2 class="section-title">Solo Projects</h2>
<div class="projects-grid">
  {% for project in solo %}
    {% include project-card.html project=project %}
  {% endfor %}
</div>
{% endif %}

{% if prototypes.size > 0 %}
<h2 class="section-title">Prototypings</h2>
<div class="projects-grid">
  {% for project in prototypes %}
    {% include project-card.html project=project %}
  {% endfor %}
</div>
{% endif %}

{% if others.size > 0 %}
<h2 class="section-title">Others</h2>
<div class="projects-grid">
  {% for project in others %}
    {% include project-card.html project=project %}
  {% endfor %}
</div>
{% endif %}