---
---

{% assign qs = site.data.questions %}
{% assign arry = "" | split: "" %}
{% for q in (1..129) %}
  {% assign key = q | prepend: "q-" %}
  {% for rs in qs[key].refs %}
    {% for r in rs %}
      {% assign arry = arry | push: r %}
    {% endfor %}
  {% endfor %}
{% endfor %}

<ol>
  {%- for r in arry -%}
    <li>{{ r }}</li>
  {%- endfor %}
</ol>
