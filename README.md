goLogParse
==========
Parse nginx-style access logs

Introduction
============

There are numerous tools and systems for parsing and visualizing data from
nginx/apache style access logs, such as the proprietary 'nginx Plus' and
luameter, logstash -> Elasticsearch/Beats/Graphite, and a number of SaaS
vendors, such as Datadog, Librato, ServerDensity, etc.

For our purposes, however, we just need a small utility to report the
distribution of HTTP response codes from our server over a period of time. The
overhead of running HTTP servers, or shipping bulk data off-site is unnecessary.

Background
==========

While the excellent (and open-source) 'ngxtop' utility accomplishes our needs,
we would like to minimize the *runtime* dependencies as much as possible.

For this reason, we've created a small, statically-compiled go binary that allows
us to parse and report on status codes.

Usage
=====

./goparselog
