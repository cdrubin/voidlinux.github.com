---
layout: default
title: Enter the void
---

<div class="container">
        <div class="row">
                <div class="col-md-4">
                        <h3>Not a fork!</h3>
                        <p>Void Linux is an independent distribution, developed entirely by volunteers.</p>
			<p>Unlike trillions of other existing distros, Void is not a modification of an existing distribution.  Void's package manager and build system have been written from scratch.</p>
		</div>
                <div class="col-md-4">
                        <h3>Rolling release</h3>
			<p>Install once, update daily. Your system will always be up-to-date.</p>
			<p>Thanks to our <a href="http://build.voidlinux.eu">continuous build system</a>, new software is built into binary packages as soon as the changes are pushed to the <em>void-packages</em> repository.</p>
		</div>
		<div class="col-md-4">
			<h3>runit</h3>
			<p>We use <a href="http://smarden.org/runit/">runit</a> as the init system and service supervisor.</p>
			<p>runit is a simple and effective approach to initialize the system with reliable service supervision. See the <a href="/usage/runit">usage page</a> for a brief introduction.</p>
		</div>
	</div>
        <div class="row">
                <div class="col-md-4">
                        <h3>LibreSSL</h3>
                        <p>We were the first distribution to switch to <em>LibreSSL</em> by default, replacing <em>OpenSSL</em>.</p>
			<p>Due to the <a href="http://en.wikipedia.org/wiki/Heartbleed">Heartbleed</a> fiasco with the <a href="http://www.openssl.org">OpenSSL</a> project we believe that <em>pro-active</em> developers are justified in seeking a more secure alternative.</p>
		</div>
                <div class="col-md-4">
                        <h3>xbps</h3>
			<p><a href="https://github.com/voidlinux/xbps">xbps</a> is the native system package manager, written from scratch with a <em>2-clause BSD</em> license.</p>
			<p><em>xbps</em> allows you to quickly install/update/remove software in your system and features detection of <em>incompatible shared libraries</em> and <em>dependencies</em> while updating or removing packages (among others). See the <a href="/usage/xbps/">usage page</a> for a brief introduction.</p>
		</div>
		<div class="col-md-4">
			<h3>xbps-src</h3>
			<p><a href="https://github.com/voidlinux/void-packages">xbps-src</a> is the xbps package builder, written from scratch with a <em>2-clause BSD</em> license.</p>
			<p>This builds the software in <em>containers</em> through the use of <em>Linux namespaces</em>, providing isolation of processes and bind mounts (among others). No root required!</p>
			<p>Additionally xbps-src can build natively or cross compile for the target machine, and supports multiple <em>C libraries</em> (glibc and musl currently).</p>
		</div>
	</div>
	<hr>
	<div class="row">
		<div class="col-md-4">
			<a class="twitter-timeline" data-chrome="noborders noscrollbar transparent" width="520" height="300" href="https://twitter.com/VoidLinux" data-widget-id="621226324586328064">Tweets by @VoidLinux</a>
			<script>!function(d,s,id){var js,fjs=d.getElementsByTagName(s)[0],p=/^http:/.test(d.location)?'http':'https';if(!d.getElementById(id)){js=d.createElement(s);js.id=id;js.src=p+"://platform.twitter.com/widgets.js";fjs.parentNode.insertBefore(js,fjs);}}(document,"script","twitter-wjs");</script>
		</div>
		<div class="col-md-4">
			<h3>void-packages changes <span class="rssdev"><a href="https://github.com/voidlinux/void-packages/commits/master.atom" title="Subscribe to void-packages"><i class="fa fa-rss fa-lg"></i></a></span></h3>
			<script src="{{site.url}}/assets/js/voidcommits.js"></script>
			<script src="https://api.github.com/repos/voidlinux/void-packages/commits?page=1&amp;per_page=10&amp;callback=voidcommits&amp;sha=master"></script>
		</div>
		<div class="col-md-4">
			<h3>xbps changes <span class="rssdev"><a href="https://github.com/voidlinux/xbps/commits/master.atom" title="Subscribe to xbps"><i class="fa fa-rss fa-lg"></i></a></span></h3>
			<script src="{{site.url}}/assets/js/voidcommits.js"></script>
			<script src="https://api.github.com/repos/voidlinux/xbps/commits?page=1&amp;per_page=10&amp;callback=voidcommits&amp;sha=master"></script>
		</div>
	</div>
	<hr>
	<div class="page-header">
		<h2>Recent news <a href="/atom.xml" title="Subscribe to the news"><i class="fa fa-rss fa-lg"></i></a></h2>
	</div>
	<div class="row">
			{% for post in site.posts limit:2 %}
			<div class="col-md-10">
				<h4>{{ post.date | date: "%B %d, %Y" }}</h4>
				<h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
				{{ post.content }}
			</div>
			{% endfor %}
	</div>
</div>
