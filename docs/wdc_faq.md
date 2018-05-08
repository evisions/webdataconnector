---
title: Frequently Asked Questions
layout: docs
---

* TOC
{:toc}

### Where can I find known issues?

You can view open issues, and submit new issues, on our [Github issues
page](https://github.com/evisions/webdataconnector/issues).

### Can I contact Evisions for help with my connector?

Evisions does not provide baseline support for connectors or for other programs written to interface with the WDC API. However,
our Professional Services department can [provide a quote](mailto:support@evisions.com) for a customized connector that meets
your needs.

If you find an issue with the WDC library, the simulator, or any of the developer samples,
 [submit an issue on Github](https://github.com/evisions/webdataconnector/issues).

### The global variables in my connector display as undefined. What's happening?

The WDC API runs connectors in multiple phases, and each phase runs in a separate instances of a web browser. To pass
data between phases, use the `tableau.connectionData` variable created by the API for this purpose. For more
information, see the documentation for the [phases of the web data connector]({{ site.baseurl }}/docs/wdc_phases.html).

### Why aren't my connector methods being called?

The methods in your connector code are run by the WDC API. Ensure that you are running the connector in the simulator or
MAPS. You might also want to ensure that the `tableau.submit` function is being called either by user input or by a
page load event.

### Can I get the links in my WDC in MAPS to open in an external browser?

Why yes, yes you can! Just add the
`target="_blank"` property to the anchor element in your web page and it will open in the user's default browser instead
of opening in MAPS. For example, you might enter the following link:

```
html <a href="http://tabsoft.co/wdc" target="_blank">Hello Docs!</a>
```
