---
layout: base.11ty.js
classes:
  - title-page
order: 3
outputs:
  - pdf
  - epub
toc: false
---

<section class="title-block">

{%- if publication.title -%}
  <h1 class="title">{{ publication.title | markdownify }}{% if publication.subtitle %}: <div class="subtitle">{{ publication.subtitle | markdownify }}</div>{% endif %}
  </h1>
{%- endif -%}

{%- if publication.contributor_as_it_appears -%}
  <p class="contributor">{{ publication.contributor_as_it_appears | markdownify }}</p>
{%- else -%}
  <p class="contributor">{% contributors context=publicationContributors type="primary" format="string" %}</p>
{%- endif -%}

</section>

<section class="publisher-block">
  <p class="publisher">Mayer Center for Ancient and Latin American Art at&nbsp;the&nbsp;Denver&nbsp;Art&nbsp;Museum, Denver, CO</p>
</section>
