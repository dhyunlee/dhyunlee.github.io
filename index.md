---
layout: single
author_profile: false
classes: wide
---

<style>
/* This page has no left sidebar and no table-of-contents, but the theme still
   reserves a gutter for each. Reclaim both so the content fills the container. */
@media (min-width: 1024px) {
  .page {
    float: none;
    width: 100%;
    padding-right: 0;
  }
}

/* Cap line length for readability - full 1280px lines are too long to read
   comfortably. Raise or remove this number to go wider. */
.page__content { max-width: 56em; }

.profile-header {
  display: flex;
  gap: 2em;
  align-items: flex-start;
  flex-wrap: wrap;
  margin-bottom: 2.5em;
}
.profile-left {
  flex: 0 0 200px;
  max-width: 200px;
}
.profile-photo {
  width: 100%;
  border-radius: 50%;
  display: block;
}
.profile-links {
  list-style: none;
  padding: 0;
  margin: 1.2em 0 0;
  font-size: 0.8em;
}
.profile-links li { margin-bottom: 0.5em; }
.profile-links a { text-decoration: none; }
.profile-name {
  margin-top: 0 !important;
  margin-bottom: 0.15em;
  border-bottom: 0;
}
.profile-title {
  color: #7a8288;
  font-size: 0.95em;
  margin: 0 0 1em;
}
.profile-bio { flex: 1 1 340px; }
@media (max-width: 600px) {
  .profile-left { flex: 0 0 150px; max-width: 150px; margin: 0 auto; }
  .profile-bio { flex: 1 1 100%; }
}
</style>

<div class="profile-header">
  <div class="profile-left">
    <img class="profile-photo" src="{{ site.author.avatar | relative_url }}" alt="{{ site.author.name }}" />
    <ul class="profile-links">
      {% if site.author.location %}
        <li><i class="fas fa-fw fa-map-marker-alt"></i> {{ site.author.location }}</li>
      {% endif %}
      {% if site.author.email %}
        <li><a href="mailto:{{ site.author.email }}"><i class="fas fa-fw fa-envelope-square"></i> Email</a></li>
      {% endif %}
      {% for link in site.author.links %}
        {% if link.url and link.label != "Email" %}
          <li><a href="{{ link.url }}" rel="me"><i class="{{ link.icon }}"></i> {{ link.label }}</a></li>
        {% endif %}
      {% endfor %}
    </ul>
  </div>

  <div class="profile-bio">
    <h1 class="profile-name">{{ site.author.name }}</h1>
    <p class="profile-title">Ph.D. Student, Computer Science &middot; George Mason University</p>
    <p>I work on the reliability of embodied AI systems. My research starts from a simple question: when a hardware fault corrupts a computation inside a large robot policy, does the robot actually fail?</p>
    <p>A vision-language-action model runs hundreds of inferences per task inside a closed feedback loop, and that loop absorbs many errors on its own. I study which faults it absorbs, which it cannot, and how to build protection that spends its budget only where it matters.</p>
  </div>
</div>

## Research interests

- Fault injection and error propagation in vision-language-action models
- Selective protection and fault tolerance for edge AI accelerators
- Model compression for on-robot deployment

## Education

- **Ph.D. in Computer Science**, George Mason University — in progress
- **M.S. in Computer Science**, George Mason University, 2026
- **M.S. in Electrical Engineering**, University of Virginia, 2023

Feel free to get in touch at [dh1120.lee@gmail.com](mailto:dh1120.lee@gmail.com).
