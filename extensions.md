---
title: Extensions
---

Chassis has a system of add-ons, just like WordPress' plugins. Extensions can install additional software inside your Chassis box, configure WordPress for certain tasks, or set up additional web services to match your production environment.

[Learn how to install extensions](http://docs.chassis.io/en/latest/extend/).

[Add your extension to the list](https://github.com/Chassis/chassis.io/blob/master/_data/extensions.yaml)

<p><label>
	Filter extensions:
	<input type="search" id="extension-filter" />
</label></p>

<div id="extension-grid" class="card-grid">
	{% for extension in site.data.extensions %}
		<div class="card extension" data-name="{{ extension.name }}" data-description="{{ extension.description }}">
			<h3>{{ extension.name }}</h3>
			<p>
				<i class="fa fa-github"></i>
				<a href="https://github.com/{{ extension.repository }}">
					{{ extension.repository }}
				</a>
			</p>
			<p class="content">
				{{ extension.description }}
			</p>
			<!-- <a href="chassis://install-extension/{{ extension.repository }}" class="button">
				<i class="fa fa-download"></i>
				Install with Chassis Desktop
			</a> -->
		</div>
	{% endfor %}
</div>

<script>
document.addEventListener( 'DOMContentLoaded', function () {
	var grid = document.getElementById('extension-grid');
	var extensions = grid.querySelectorAll('.extension');
	document.getElementById('extension-filter').addEventListener('input', function (e) {
		var value = e.target.value.toLowerCase();
		extensions.forEach(function (element) {
			var name = element.dataset.name.toLowerCase() + " " + element.dataset.description.toLowerCase();
			element.classList.toggle('no-match', name.indexOf( value ) === -1);
		});
	});
});
</script>
