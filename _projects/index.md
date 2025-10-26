---
layout: default
title: "Projects"
permalink: /projects/
---

<h1 style="text-align: center; margin-bottom: 40px;">My DSCI and GIS Projects</h1>

<div class="projects-grid">
  {% assign sorted_projects = site.projects | sort: "order" | reverse %}
  {% for project in sorted_projects %}
    {% if project.title != "Projects" %}
      <div class="project-card">
        <a href="{{ project.url | relative_url }}">
          <img src="{{ project.image | relative_url }}" alt="{{ project.title }}" class="project-thumb">
        </a>
        <h3>{{ project.title }}</h3>
        <p>{{ project.intro }}</p>
      </div>
    {% endif %}
  {% endfor %}
</div>
