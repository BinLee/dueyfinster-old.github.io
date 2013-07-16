---
layout: post
title: "SSH Config Aliases"
description: ""
category: 
tags: []
---
{% include JB/setup %}

If your like me and you deal with a lot of servers for development or test and do it from a Unix machine, I've got a really handy tip: SSH hostname pattern matching.

Say I've got a SSH config file like this (at <span style="font-family: &quot;Courier New&quot;,Courier,monospace;">~/.ssh/config</span>):

<script src="https://gist.github.com/dueyfinster/5822509.js"></script>

The ssh man page explains this really well:
<blockquote>
<p> A pattern consists of zero or more non-whitespace characters, '*' (a
     wildcard that matches zero or more characters), or '?' (a wildcard that
     matches exactly one character).  For example, to specify a set of decla-
     rations for any host in the ``.co.uk'' set of domains, the following pat-
     tern could be used:</p> 

           <p>Host *.co.uk</p> 

     <p>The following pattern would match any host in the 192.168.0.[0-9] network
     range:</p> 

          <p> Host 192.168.0.?</p> 

     <p>A pattern-list is a comma-separated list of patterns.  Patterns within
     pattern-lists may be negated by preceding them with an exclamation mark
     ('!').  For example, to allow a key to be used from anywhere within an
     organisation except from the ``dialup'' pool, the following entry (in
     authorized_keys) could be used:</p> 

           from="!*.dialup.example.com,*.example.com"</p>
</blockquote>

So there you have it!