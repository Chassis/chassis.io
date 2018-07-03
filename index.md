---
body_id: home
layout: home
---
<header>
	<div class="wrap">
		<div class="title">
			<img
				src="{{ site.baseurl }}images/logo-128.png"
				srcset="{{ site.baseurl }}images/logo-128.png 1x, {{ site.baseurl }}images/logo-256.png 2x"
			/>
			<h1>Develop WordPress Sites Locally with
				<strong>Chassis</strong></h1>
		</div>

		<!-- <img
			src="{{ site.baseurl }}images/main.png"
			srcset="{{ site.baseurl }}images/main.png 1x, {{ site.baseurl }}images/main@2x.png 2x"
		/> -->

		<div class="get">
			<div class="desktop">
				<a href="//github.com/Chassis/Desktop/releases/tag/0.2.0" class="download">
					<i class="fa fa-download"></i>
					<span>
						<span class="main">Download Chassis Desktop</span>
						<span class="details">v0.2.0, released 24 May 2017</span>
					</span>
				</a>
			</div>

			<div class="vagrant">
				<p>Familiar with Vagrant? Download the box.</p>
				<a href="//github.com/Chassis/Chassis" class="download">
					<i class="fa fa-code-fork"></i>
					<span>
						<span class="main">Clone Chassis Box</span>
						<span class="details">Requires Vagrant 1.7+</span>
					</span>
				</a>
			</div>
		</div>

		<div class="cutoff"></div>
	</div>
</header>

<section class="wrap block">
	<div>
		<h2>Match your production servers&nbsp;locally.</h2>
		<p>Configure Chassis to run the same version of PHP as your production servers, including PHP extensions. Never hear &ldquo;it worked on my machine!&rdquo;&nbsp;again.</p>
	</div>
	<pre class="terminal">
Welcome to Ubuntu 12.04 LTS (GNU/Linux 3.2.0-23-generic x86_64)
Last login: Sat Nov 19 14:16:24 2016 from 10.0.2.2
vagrant@vagrant:~$ php --version
PHP 5.6.22-1+donate.sury.org~precise+1 (cli)
Copyright (c) 1997-2016 The PHP Group
Zend Engine v2.6.0, Copyright (c) 1998-2016 Zend Technologies
    with Zend OPcache v7.0.6-dev, Copyright (c) 1999-2016, by
      Zend Technologies
vagrant@vagrant:~$ mysql --version
mysql  Ver 14.14 Distrib 5.5.49, for debian-linux-gnu (x86_64)
  using readline 6.2
vagrant@vagrant:~$ nginx -v
nginx version: nginx/1.1.19</pre>
</section>

<section class="wrap block reverse">
	<div>
		<h2>Built for everyone.</h2>
		<p>We built Chassis Desktop as an easy-to-use UI for everyone from developers to designers to project managers, beginners to experts.</p>
		<p>But it doesn&lsquo;t stop there. We&lsquo;ve filled Desktop with power-user tools, like keyboard navigation: just hold &#x2318; to view shortcuts.</p>
		<p>Need more control? Drop down to the terminal and work directly with Vagrant.</p>
	</div>
	<div>
		<img
			class="mac-screenshot"
			src="{{ site.baseurl }}images/keyboard.png"
			srcset="{{ site.baseurl }}images/keyboard.png 1x, {{ site.baseurl }}images/keyboard@2x.png 2x"
		/>
	</div>
</section>

<section class="wrap block">
	<div>
		<h2>Extensible <abbr title="as Frasier">AF</abbr></h2>
		<p>We can&lsquo;t be everything to everyone. Fortunately, with Chassis&lsquo; ecosystem of extensions, you can build a system to your exact specifications.</p>
		<a class="button" href="{{ site.baseurl }}extensions/">
			<i class="fa fa-puzzle-piece"></i>
			View all {{ site.data.extensions|size }} extensions
			&rarr;
		</a>
	</div>
	<div class="extension card">
		<h3>Memcache</h3>
		<p>
			<i class="fa fa-github"></i>
			<a href="https://github.com/Chassis/Memcache">
				Chassis/Memcache
			</a>
		</p>
		<p class="content">
			Install memcache and add it to PHP (uses PECL memcache).
		</p>
		<!--
		<a href="chassis://install-extension/Chassis/Memcache" class="button">
			<i class="fa fa-download"></i>
			Install with Chassis Desktop
		</a>
		-->
	</div>
</section>

<section class="wrap block reverse">
	<div>
		<h2>Open Source, natch.</h2>
		<p>Just like WordPress, Chassis is 100% open source, with <a href="https://github.com/Chassis/Chassis/graphs/contributors">20+ independent contributors</a>. Chassis is a community project, with commercial support from <a href="https://hmn.md/">Human Made</a>.</p>
	</div>
	<div class="github-card">
		<a class="header" href="https://github.com/Chassis/Chassis">
			<h3>Chassis/Chassis</h3>
			<i class="fa fa-github"></i>
		</a>
		<p class="contributors">
			<a href="https://github.com/Chassis/Chassis/graphs/contributors">
				<i class="fa fa-users"></i>
				<strong id="gh-contributors">26</strong> contributors
			</a>
			<a href="https://github.com/Chassis/Chassis/graphs/network">
				<i class="fa fa-code-fork"></i>
				<strong id="gh-forks">70</strong> forks
			</a>
		</p>
		<a class="star ghbtn" href="https://github.com/Chassis/Chassis/stargazers">
			<span><i class="fa fa-star"></i> Star</span><span id="gh-stars">422</span>
		</a>
		<a class="watch ghbtn" href="https://github.com/Chassis/Chassis/watchers">
			<span><i class="fa fa-eye"></i> Watch</span><span id="gh-watchers">35</span>
		</a>
	</div>
</section>

<section class="start">
	<div class="wrap">
		<h2>Ready to get started?</h2>
		<div class="button-wrap">
			<a href="//github.com/Chassis/Desktop" class="download">
				<i class="fa fa-download"></i>
				<span>
					<span class="main">Download Chassis Desktop</span>
					<span class="details">v1.0, releasing soon</span>
				</span>
			</a>
			<a href="//github.com/Chassis/Chassis" class="download">
				<i class="fa fa-code-fork"></i>
				<span>
					<span class="main">Clone Chassis Box</span>
					<span class="details">Requires Vagrant 1.7+</span>
				</span>
			</a>
		</div>
	</div>
</section>

<script>
	function ghJsonpCallback( response ) {
		var data = response.data;
		document.getElementById('gh-forks').textContent = data.forks_count;
		document.getElementById('gh-stars').textContent = data.stargazers_count;
		document.getElementById('gh-watchers').textContent = data.subscribers_count;
		console.log( data );
		return null;
	}

	document.addEventListener( 'DOMContentLoaded', function () {
		var scriptEl = document.createElement( 'script' );
		scriptEl.src = 'https://api.github.com/repos/Chassis/Chassis?callback=ghJsonpCallback';
		document.body.appendChild( scriptEl );
	});
</script>
