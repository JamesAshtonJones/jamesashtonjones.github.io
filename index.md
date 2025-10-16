---
layout: home
title: Home
---

<div id="intro-wrapper" class="l-text">
	<div id="intro-title-wrapper">
		<div id="intro-title-text-wrapper">
			<h1 id="intro-title">James Ashton Jones</h1>
			<div id="intro-subtitle">Student at Georgia Tech</div>
			<div id="intro-title-socials">
				{% for link in site.data.social-links %}
					{% if link.on-homepage == true %}
						{% include social-link.html link=link %}
					{% endif %}
				{% endfor %}
			</div>
		</div>
		<div id="intro-image-wrapper">
			<img id="intro-image" src="/images/casual.jpg">
		</div>
	</div>
	<div id="everything-else" class="l-middle">
		<a href="/resume.pdf"><div><i class="fa fa-portrait icon icon-right-space"></i>Resume</div></a>
		<a href="/projects"><div><i class="fas fa-laptop-code icon icon-right-space"></i>Projects</div></a>
		<a href="{{ site.url }}/everything-else"><div><i class="fa fa-list-ul icon icon-right-space"></i>Everything Else</div></a>
	</div>
	<hr class="l-middle home-hr">
	<div>
		Hi! I'm Ashton, and I'm interested in data science, math modeling, and quantitative finance.
	</div>
</div>

<hr class="l-middle home-hr">

<!-- <h2 class="feature-title">Featured <a href="/projects">Projects</a></h2> -->
<h2 class="feature-title">Featured Projects</h2>

<div class="cover-wrapper cover-wrapper-3-col l-page">
	{% assign sortedPublications = site.categories.projects | sort: 'feature-order' %}
	{% for feature in sortedPublications %}
		{% if feature.featured == true %}
			{% include feature.html feature=feature %}
		{% endif %}
	{% endfor %}
</div>

<div id="everything-else" class="see-all">
	<a href="/projects"><div>See All Projects ►</div></a>
</div>
