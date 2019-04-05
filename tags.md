---
layout: page
title: Tags
permalink: /tags/
sitemap:
  priority: 0.7
---
<h1 style="display:inline;">랜덤 태그: </h1>
<h1 style="display:inline;">
    <a href="" id="tagLink"></a>
</h1>
<script type="text/javascript">
	var allTags = [{% for tag in site.tags %}"{{ tag.name | escape }}",{% endfor %}""];
	allTags.pop();
	var tag = document.getElementById("tagLink");
	var random = Math.floor(Math.random() * allTags.length);
    tag.href = "{{ site.baseurl }}/tags/"+allTags[random];
    tag.innerHTML = allTags[random];
</script>
{% for tag in site.tags %}
* [{{ tag.name }}]({{ site.baseurl }}/tags/{{ tag.name }})
{% endfor %}