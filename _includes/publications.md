<h2 id="publications" style="margin: 10px 0px -10px;">Publications</h2>

<div class="publications">
<ol class="bibliography">

{% for pub in site.data.publications.main %}

<li>
  <div class="pub-row">

    <!-- Thumbnail / Badge -->
    <div class="col-sm-3 abbr" style="padding-right:15px;">
      {% if pub.image %}
        <img src="{{ pub.image }}" class="teaser img-fluid z-depth-1" style="width:100%; max-width:260px; height:auto;">
        {% if pub.conference_short %}
          <abbr class="badge">{{ pub.conference_short }}</abbr>
        {% endif %}
      {% endif %}
    </div>

    <!-- Paper Info -->
    <div class="col-sm-9" style="padding-left:20px;">
      <div class="title">
        {% if pub.pdf %}
          <a href="{{ pub.pdf }}" target="_blank">{{ pub.title }}</a>
        {% else %}
          {{ pub.title }}
        {% endif %}
      </div>

      <div class="author">{{ pub.authors }}</div>

      <div class="periodical">
        <em>{{ pub.conference }}</em>
      </div>

      <!-- Action Buttons -->
      <div class="links">
        {% if pub.pdf %}
          <a href="{{ pub.pdf }}" class="btn btn-sm z-depth-0" target="_blank">PDF</a>
        {% endif %}
        {% if pub.code %}
          <a href="{{ pub.code }}" class="btn btn-sm z-depth-0" target="_blank">Code</a>
        {% endif %}
        {% if pub.page %}
          <a href="{{ pub.page }}" class="btn btn-sm z-depth-0" target="_blank">Project Page</a>
        {% endif %}
        {% if pub.bibtex %}
          <a href="{{ pub.bibtex }}" class="btn btn-sm z-depth-0" target="_blank">BibTeX</a>
        {% endif %}
        {% if pub.notes %}
          <strong><i style="color:#e74d3c;">{{ pub.notes }}</i></strong>
        {% endif %}
      </div>
    </div>

  </div>
</li>

{% endfor %}

</ol>
</div>
