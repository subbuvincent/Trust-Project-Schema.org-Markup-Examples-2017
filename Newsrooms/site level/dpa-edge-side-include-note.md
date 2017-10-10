# Edge Side Includes

One light-weight way of including site-level metadata into your HTML can be Edge-Side-Includes.

This is a not yet standardized way of "including" stuff from
other servers into your websites. This option can solve a
problem if access to the templates for the generated HTML is
not easily possible and / or if the system used to update
the site-wide metadata is decoupled from the CMS. By
including a tag like the one below, you can "include" the
markup in the page.

```HTML

<esi:include src="http://example.com/site-wide-trust-project-markup-v1.1.json" onerror="continue"/>

```

It's documented quite reasonably [in the Wikipedia
article](https://en.wikipedia.org/wiki/Edge_Side_Includes).
It is ony advisable to consider using Edge Side Includes if
you have the builing blocks that support it already in your
infrastructure: either a supporting caching proxy servers
such as Varnish, Squid and Mongrel ESI or the services of a
Content Delivery Network such as Akamai or Cloudflare.

This "include" paradigm also can work on the server (please
google Server Side Includes). 
