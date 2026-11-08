<h2 id="projects" class="pub-section-title">Projects</h2>

<div class="publications projects">
<ol class="bibliography">

{% for link in site.data.projects.main %}

<li>
<div class="pub-row">
  <div class="col-sm-3 abbr project-media" style="position: relative;padding-right: 15px;padding-left: 15px;">
    {% if link.video %}
    <video class="teaser project-video" src="{{ link.video }}" muted loop playsinline preload="metadata"></video>
    <img src="{{ link.image }}" class="project-cover" alt="">
    <span class="video-spinner" aria-hidden="true"></span>
    <span class="play-hint" aria-hidden="true"><i class="fa fa-play"></i></span>
    {% elsif link.image %}
    <img src="{{ link.image }}" class="teaser img-fluid z-depth-1">
    {% else %}
    <div class="project-placeholder"><i class="fa fa-film"></i><span>Demo coming soon</span></div>
    {% endif %}
  </div>
  <div class="col-sm-9" style="position: relative;padding-right: 15px;padding-left: 20px;">
      <div class="title">{{ link.title }}</div>
      <div class="project-role"><strong>{{ link.role }}</strong>{% if link.period %} · {{ link.period }}{% endif %}</div>
      {% if link.collaboration %}<div class="periodical"><em>{{ link.collaboration }}</em></div>{% endif %}
      {% if link.description %}<div class="project-desc">{{ link.description }}</div>{% endif %}
      {% if link.contributions %}
      <ul class="project-contrib">
        {% for c in link.contributions %}<li>{{ c }}</li>{% endfor %}
      </ul>
      {% endif %}
  </div>
</div>
</li>

{% endfor %}

</ol>
</div>
