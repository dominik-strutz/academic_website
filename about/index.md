---
title: About
banner_image: images/backgrounds/cornwall_cliffs_1.jpg
banner_position: center center
banner_title: About me
banner_subtitle: A bit more about me and my work
template: base.html
---

{% from "macros.html" import figure %}

<section class="mb-5">

## The slightly longer version

My passion for the planet beneath our feet is what brought me into geophysics. The combination of classical mechanics, fascinating geological processes and high-performance computing applied to usually inaccessible structures is what keeps me fascinated to this day. Exactly this inaccessibility makes inverse problems - converting data to models of the subsurface - so vital to geophysics. Any optimization in this process will lead to a better understanding of the world around us.

Most of the time, data is taken as given in inverse problems. In my project, I take a step back and investigate how much the design of an experiment can influence the expected results. The next step is then how to choose an experiment that is most likely optimal in the sense of giving the most information about the subsurface given a typical dataset.

While based on a straightforward theoretical framework, solving this problem in practice is computationally very expensive, if not infeasible, even for relatively small-scale experiments. My work over the following years will mainly focus on finding approximations that allow designing extensive surveys of one or several sensor types optimally. 

After finding these methods, I will focus my research on how to design experiments to answer specific questions such as: "What's the size of a certain subsurface body?" or "Is the source of micro-seismicity moving upwards?" 

All of the methods I plan on using extensively use concepts from statistics and machine learning, and I am very excited to learn more about those to complement my geophysics background.

Finally, I want to thank the [SPIN-project][spin] for giving me the unique opportunity to work on this project as part of a Marie Skłodowska-Curie Actions EU grant. 

<!-- {{ figure("../images/teaching-git-at-agu2019.jpg", 'Me teaching git and GitHub at <a href="https://github.com/agu-ossi/2019-agu-oss">AGU2019</a>.', class="mt-4") }} -->


<!-- </section>
<section class="mb-5">

<h2>Online</h2>

<!-- Find out more about me and my work at:

{%- macro social_button(link, icon, name) -%}
  <a class="btn btn-outline-light me-2 mb-3" target="_blank" href="{{ link }}"><i class="{{ icon }} me-1" aria-hidden="true"></i> {{ name }}</a>
{%- endmacro -%}

<div id="social-links">
{{ social_button("https://github.com/" ~ config.github, icon="fab fa-github", name="GitHub") }}
{{ social_button("https://twitter.com/" ~ config.twitter, icon="fab fa-twitter", name="Twitter") }}
{{ social_button(config.linkedin, icon="fab fa-linkedin", name="LinkedIn") }} -->
<!-- {{ social_button(config.youtube, icon="fab fa-youtube", name="YouTube") }}
{{ social_button("https://orcid.org/" ~ config.orcid, icon="ai ai-orcid", name="ORCID") }}
{{ social_button("https://profiles.impactstory.org/u/" ~ config.orcid, icon="ai ai-impactstory", name="ImpactStory") }} -->
<!-- {{ social_button("http://figshare.com/authors/Leonardo%20Uieda/97471", icon="ai ai-figshare", name="figshare") }} -->
<!-- {{ social_button(config.googlescholar, icon="ai ai-google-scholar", name="Google Scholar") }} -->
<!-- {{ social_button(config.publons, icon="ai ai-publons", name="Publons") }}
{{ social_button(config.researchgate, icon="ai ai-researchgate", name="ResearchGate") }} -->
<!-- </div> -->
<!-- </section> -->

<section class="mb-5">

<h2 id="cv">Curriculum Vitae</h2>

I keep a full length version of my CV updated and publicly available:

<!-- #TODO: Insert CV -->
<a class="btn btn-primary mb-3" href="..\pdf\Master_Thesis_Dominik_Strutz.pdf" target="_blank" type="application/pdf" rel="external noopener noreferrer">
<i class="me-1 fa fa-download" aria-hidden="true"></i>
Download my CV in PDF
</a>

<!-- <div class="callout mt-3">

**Curious about the CV template?** It's typeset in LaTeX using a custom
template. The source is available from the GitHub repository
<a class="nowrap" href="https://github.com/leouieda/cv"><i class="mx-1 fab fa-github" aria-hidden="true"></i><code>leouieda/cv</code></a>.

</div> -->

</section>
<section class="mb-5">

## Education

{% import "macros.html" as macros %}

{# The education list is defined in about/data.yml #}
{% for item in page.education %}

<div class="mb-3">
{%- set id = loop.index %}
<h2 class="fs-4 mb-1">
  {{ item.level|trim }}
</h2>
<p class="mb-1">
  <span class="text-muted">{{ item.year }}</span>
  |
  {{ item.institution|trim }}
</p>
<p class="mb-1 text-muted fs-6">
  Thesis: {{ item.title|trim }}
</p>
<p class="mb-1 text-muted fs-6">
  Advisor: {{ item.advisor }}
</p>
<!-- <p class="text-muted fs-6">
  doi:<a href="https://doi.org/{{ item.doi }}">{{ item.doi }}</a>
</p> -->
<button class="btn btn-secondary btn-sm me-1 mb-2" type="button"
    data-bs-toggle="collapse" data-bs-target="#collapse-abstract-{{ id }}"
    aria-expanded="false" aria-controls="collapse-abstract-{{ id }}">
  Find out more <i class="fa fa-chevron-circle-down ms-1" aria-hidden="true"></i>
</button>
<!-- {{ macros.button_link("https://doi.org/" ~ item.doi, "PDF", type="btn-primary", icon="fa fa-file-pdf") }} -->
<!-- {{ macros.button_link("https://github.com/" ~ item.github, "Code", type="btn-light", icon="fab fa-github") }} -->
{{ macros.button_link(item.slides, "Slides", type="btn-light", icon="fa fa-desktop") }}
<div id="collapse-abstract-{{ id }}" class="collapse paper-info mt-2 overflow-hidden">
  <!-- <h3 class="">About</h3>
  {{ item.notes }} -->
  <h3 class="">Abstract</h3>
  <p>{{ item.abstract|trim }}</p>
</div>
</div>

{% endfor %}

</section>


[spin]: https://spin-itn.eu/

