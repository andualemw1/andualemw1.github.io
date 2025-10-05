---
layout: default
title: "Publications"
permalink: /publications/
---

<div class="page-container">

  <header class="page-header">
    <h1>Publications</h1>
  </header>

  <section class="page-content">
    {% for pub in site.publications reversed %}
      <div class="publication-entry" style="margin-bottom: 2rem;">
        <h3>{{ pub.title }}</h3>
        <p><strong>{{ pub.authors }}</strong></p>
        <p><em>{{ pub.venue }}, {{ pub.date | date: "%Y" }}</em></p>
        <div class="publication-links">
          {% if pub.pdf %}<a href="{{ pub.pdf }}" class="btn btn-secondary" target="_blank">[PDF]</a>{% endif %}
          {% if pub.code %}<a href="{{ pub.code }}" class="btn btn-secondary" target="_blank">[Code]</a>{% endif %}
          {% if pub.project %}<a href="{{ pub.project }}" class="btn btn-secondary" target="_blank">[Project Page]</a>{% endif %}
        </div>
      </div>
    {% endfor %}
  </section>

</div>

