{% unless include.query == falsy %}
{% for person in project_info.manpower.personnel %}
  {% for role in person.roles %}
    {% if role == include.query %}
      - {{ person.name }} <a href="{{ person.github_link }}">({{ person.username }}) </a> <br>
    {% endif %}
  {% endfor %}
{% endfor%}
{% endunless %}
