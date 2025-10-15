---
layout: page
title: Projects
permalink: projects/
---

Things I've worked on, as part of research, courses, or just on the side.

<hr>

<div class="cover-wrapper cover-wrapper-3-col l-page">
	{% assign sortedPublications = site.categories.projects | sort: 'feature-order' %}
	{% for feature in sortedPublications %}
		{% if feature.dissertation == true %}
			{% include feature.html feature=feature %}
		{% endif %}
	{% endfor %}
</div>

<div class="project-spacer"></div>
