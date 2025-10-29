<h2 id="publications" style="margin: 2px 0px -15px;">Projects</h2>

<div class="publications">
<ol class="bibliography">

{% for link in site.data.projects.main %}

<li>
<div class="pub-row">
  <div class="col-sm-3 abbr" style="position: relative;padding-right: 15px;padding-left: 15px;">
    {% if link.image %} 
    <img src="{{ link.image }}" class="teaser img-fluid z-depth-1" style="width=100;height=40%">
    {% if link.type %} 
    <abbr class="badge">{{ link.type }}</abbr>
    {% endif %}
    {% endif %}
  </div>
  <div class="col-sm-9" style="position: relative;padding-right: 15px;padding-left: 20px;">
      <div class="title" style="font-size: 18px;"><a href="{{ link.github }}">{{ link.title }}</a></div>
      <div class="author">{{ link.authors }}</div>
      <div class="periodical"><em>{{ link.conference }}</em>
      </div>
      
      {% if link.description %}
      <div class="project-description" style="margin: 5px 0 10px 0; font-size: 16px; color: #333;">
        {{ link.description }}
      </div>
      {% endif %}

    <div class="links">
      {% if link.github %} 
      <a href="{{ link.github }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">GitHub Link</a>
      {% endif %}
      {% if link.notes %} 
      <strong> <i style="color:#e74d3c">{{ link.notes }}</i></strong>
      {% endif %}
      {% if link.others %} 
      {{ link.others }}
      {% endif %}
    </div>
  </div>
</div>
</li>
<br>

{% endfor %}

</ol>
</div>
