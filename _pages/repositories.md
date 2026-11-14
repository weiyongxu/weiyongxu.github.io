---
layout: page
permalink: /repositories/
title: repositories
description: Open-source research software and analysis code.
nav: true
nav_order: 4
---

**[rsa-nd](https://github.com/weiyongxu/rsa-nd)**

A Python package for representational similarity analysis of EEG/MEG data across sensors, brain regions, time and frequency. [DOI](https://doi.org/10.5281/zenodo.24088896)

**[Calcium Imaging Cell Sorter](https://github.com/weiyongxu/calcium_imaging_cell_sorter)**

A desktop application for reviewing cells and activity traces in Inscopix calcium-imaging recordings. [DOI](https://doi.org/10.5281/zenodo.24089476)

{% if site.data.repositories.github_users %}

## GitHub users

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for user in site.data.repositories.github_users %}
    {% include repository/repo_user.liquid username=user %}
  {% endfor %}
</div>

---

{% if site.repo_trophies.enabled %}
{% for user in site.data.repositories.github_users %}
{% if site.data.repositories.github_users.size > 1 %}

  <h4>{{ user }}</h4>
  {% endif %}
  <div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% include repository/repo_trophies.liquid username=user %}
  </div>

---

{% endfor %}
{% endif %}
{% endif %}

{% if site.data.repositories.github_repos %}

## Other repositories

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.repositories.github_repos %}
    {% include repository/repo.liquid repository=repo %}
  {% endfor %}
</div>
{% endif %}
