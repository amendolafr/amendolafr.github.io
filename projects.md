---
layout: default
title: Projects
---
[← Home]({{ '/' | relative_url }})


# Projects

Projects I've worked on:

<div class="project-grid">
  {% for p in site.data.projects %}
  <article class="project-card">
    <h3><a href="{{ p.url | default: '#' }}">{{ p.name }}</a></h3>
    <p>{{ p.summary }}</p>
    {% if p.tech %}<p><small><em>{{ p.tech | join: ", " }}</em></small></p>{% endif %}
    {% if p.links %}
      <p class="links">
        {% for l in p.links %}
          <a href="{{ l.url }}">{{ l.label }}</a>{% unless forloop.last %} · {% endunless %}
        {% endfor %}
      </p>
    {% endif %}
  </article>
  {% endfor %}
</div>
