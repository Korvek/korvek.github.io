---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
title: Portfolio
---
<h1>Game Dev Portfolio</h1>
<div class="projects-grid">
  {% for project in site.projects %}
  <a class="project-card" >	<!--href="{{ project.url | relative_url }}"-->

    <div class="card-image">
      <img src="{{ project.image | relative_url }}" alt="{{ project.title }}">
    </div>

    <div class="card-content">
      <h2>{{ project.title }}</h2>
      <p>{{ project.excerpt }}</p>
    </div>

  </a>
  {% endfor %}

</div>