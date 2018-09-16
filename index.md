---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
---

<section class="page-home">
  {% assign projects = site.work | sort: 'sequence' %}
  {% for project in projects %}
  <figure class="work-box">
    <a href="{{ project.url }}">
      <img
        src="{{ project.cover_image | relative_url }}"
      />
      <figcaption>{{ project.title }}</figcaption>
    </a>
  </figure>
  {% endfor %}
</section>
