---
layout: page
title: Stats Pattern
parent: Design Patterns
---
Stats are a list of paired properties and values that we use at the end of [meta](patterns-meta) or [blurbs](patterns-blurb) and similar descriptive blocks. They are usually countable values (e.g. Hits: 100) or some kind of binary status (e.g. Status: Complete).

The stats style is declared in [10-types-groups.css](https://github.com/otwcode/otwarchive/blob/master/public/stylesheets/site/2.0/10-types-groups.css).

* [Rules](#rules)
* [Quick reference](#quick-reference)
* [XHTML diagram](#xhtml-diagram)

<h3 id="rules">Rules</h3>

Stats are always a `dl.stats`. You can never have any other kind of stats.

Stats always come at the end of meta and work blurbs. Stats may also appear in other contexts. 

`dl.stats` <em>may</em> appear within a `dd.stats`, but it can't be depended on.

The colon should be included in the translation string, <strong>not</strong> inserted with CSS.

Property and value pairs may be given matching class names. Never give a class to the property and not the value (or vice verse).

<h3 id="quick-reference">Quick reference</h3>

<dl class="key"><dt>[...]</dt><dd>always included</dd>
<dt>{...}</dt><dd>sometimes included</dd></dl>

<pre>
[dl stats]
    [dt][/dt]
    [dd][/dd]
[/dl]
</pre>

<h3 id="xhtml-diagram">XHTML diagram</h3>

This diagram is taken from work meta.

<div class="diagram">
  <ol>
    <li><code>&lt;dl class="stats"&gt;</code>
      <ol>
        <li><code>&lt;dt class="published"&gt;</code></li>
        <li><code>&lt;dd class="published"&gt;</code></li>
        <li><code>&lt;dt class="words"&gt;</code></li>
        <li><code>&lt;dd class="words"&gt;</code></li>
        <li><code>&lt;dt class="chapters"&gt;</code></li>
        <li><code>&lt;dd class="chapters"&gt;</code></li>
        <li><code>&lt;dt class="comments"&gt;</code></li>
        <li><code>&lt;dd class="comments"&gt;</code></li>
        <li><code>&lt;dt class="kudos"&gt;</code></li>
        <li><code>&lt;dd class="kudos"&gt;</code></li>
        <li><code>&lt;dt class="hits"&gt;</code></li>
        <li><code>&lt;dd class="hits"&gt;</code></li>
      </ol>
    </li>
  </ol>
</div>
