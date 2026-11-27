
---
title: "Schäberle Lab - Research Projects"
layout: gridlay
excerpt: "Research projects of the Schäberle Lab."
sitemap: false
permalink: /projects/
---

# Research Projects

Our research projects combine microbiology, natural product chemistry, biotechnology and bioinformatics to discover and develop bioactive compounds for applications in human and animal health, agriculture and sustainable food production.

<style>
.projects-grid {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 24px;
  margin: 30px 0 45px;
}

.project-card {
  display: flex;
  flex-direction: column;
  background: #fff;
  border: 1px solid #e3e3e3;
  border-radius: 14px;
  padding: 24px;
}

.project-card h3 {
  font-size: 20px;
  font-weight: 700;
  line-height: 1.4;
  margin: 0 0 16px;
}

.project-card p {
  line-height: 1.7;
  margin-bottom: 20px;
  flex-grow: 1;
}

.project-link {
  display: inline-block;
  align-self: flex-start;
  padding: 9px 16px;
  color: #fff !important;
  background: #0087b8;
  border-radius: 6px;
  text-decoration: none !important;
  font-weight: 600;
}

.project-link:hover {
  background: #006b94;
}

@media (max-width: 767px) {
  .projects-grid {
    grid-template-columns: 1fr;
  }

  .project-card {
    padding: 18px;
  }
}
</style>

<div class="projects-grid">

{% for project in site.data.projects %}

<div class="project-card">

  <h3>{{ project.name }}</h3>

  <p>{{ project.description }}</p>

  {% if project.url and project.url != "" %}
  <a
    class="project-link"
    href="{{ project.url }}"
    target="_blank"
    rel="noopener noreferrer"
  >
    Project details
  </a>
  {% endif %}

</div>

{% endfor %}

</div>
