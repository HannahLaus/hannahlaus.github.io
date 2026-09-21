---
layout: page
permalink: /repositories/
title: repositories
description: This is the link to my Github repository.
nav: true
nav_order: 4
---

{% if site.data.repositories.github_users %}

<!--## GitHub users

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

{% if site.data.repositories.github_repos %}-->

## GitHub Repositories

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.repositories.github_repos %}
    {% include repository/repo.liquid repository=repo %}
  {% endfor %}
</div>
{% endif %}

<style>
  .repo-card {
    display: block; flex: 1 1 320px; max-width: 480px; margin: 0.5rem;
    padding: 1rem 1.25rem; border: 1px solid var(--global-divider-color);
    border-radius: 8px; background: var(--global-card-bg-color);
    color: var(--global-text-color); text-decoration: none;
    transition: border-color 0.15s, transform 0.15s;
  }
  .repo-card:hover {
    border-color: var(--global-theme-color); transform: translateY(-2px);
    text-decoration: none; color: var(--global-text-color);
  }
  .repo-card-title { font-weight: 600; color: var(--global-theme-color); }
  .repo-card-desc { margin: 0.5rem 0; font-size: 0.9rem; }
  .repo-card-meta { font-size: 0.8rem; opacity: 0.7; }
</style>
<script>
  document.querySelectorAll(".repo-card").forEach(async (card) => {
    try {
      const r = await fetch("https://api.github.com/repos/" + card.dataset.repo);
      if (!r.ok) return;
      const d = await r.json();
      card.querySelector(".repo-card-desc").textContent = d.description || "";
      const meta = [];
      if (d.language) meta.push(d.language);
      meta.push(d.stargazers_count + " stars");
      meta.push(d.forks_count + " forks");
      card.querySelector(".repo-card-meta").textContent = meta.join("  |  ");
    } catch (e) {}
  });
</script>
