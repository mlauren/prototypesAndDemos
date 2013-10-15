---
layout: post
title:  "Group-space Menus"
date:   2013-10-14 09:05:45
categories: groupspace prototype administer
---
<div class="row panel">
  <a class="extra" href="/">← home</a>
</div>
<div class="panel callout row">
	<h2 class="large-4 columns">AP Tigers</h2>
</div>
<div class="row">
	<div class="large-4 small-12 columns">
		<div class="row panel">
			<div class="large-12 columns">
				<a href="#" data-dropdown="drop2" class="small secondary radius button dropdown large-12">My Settings</a>
				<br>
				<ul id="drop2" data-dropdown-content="" class="f-dropdown" style="position: absolute; top: 72px; left: -99999px;">
		          {% for menuitem in site.menus.personalSettingsPermAdmin %}
				    <li><a href="#">{{ menuitem.title }}</a></li>
				  {% endfor %}
		        </ul>
			</div>
			<hr />
			<div class="group-image columns">
				<img src="http://placehold.it/280x280"/>
			</div>
			<div class="columns">
				<ul class="side-nav">
					<hr>
					{% for menuitem in site.menus.socialMenuPermAdmin %}
					<li class="{{ menuitem.title | replace:' ','-' | downcase }}"><a href="#">{{ menuitem.title }}</a></li>
					<hr>
					{% endfor %}
				</ul>
			</div>
			<ul class="social-share">
				<li><i class="icon-facebook-sign"></i></li>
				<li><i class="icon-tumblr"></i></li>
				<li><i class="icon-twitter"></i></li>
			</ul>
		</div>
		<div class="row panel callout">
			<h3 class="subheader"> <i class="icon-cog"></i>Admin Menu</h3>
			{% include adminmenu.snippet %}
		</div>
	</div>
</div>
