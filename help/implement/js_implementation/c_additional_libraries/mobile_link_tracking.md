---
description: null
keywords: Analytics Implementation;link reference;redir
seo-description: null
seo-title: Custom link measurement on mobile protocols
solution: Analytics
title: Custom link measurement on mobile protocols
topic: Developer and implementation
uuid: c6262a79-add6-4188-8870-48a702c2d7d3
index: y
internal: n
snippet: y
---

# Custom link measurement on mobile protocols

Many mobile device users download files to their devices such as podcasts, ring tones, and similar files. Because many mobile devices do not support JavaScript, link measurement must be implemented through redirects. To use redirects, you must modify the href links in the html to include the REDIR element. The general format for a custom link is as follows:

```
http://<your_Namespace>.112.2o7.net/b/ss/<RSID>/4/REDIR/
?url=<destination_URL>&pe=<link_type>&pev1=<current_URL>&pev2=<link_name>
```

Keep in mind the following when creating link reference:

* The URL value must be URL encoded. 
* You should set a pageName or page URL (g) parameter. 
* Dynamic variables can read the URL parameter but not set it. 
* If no cookie is set, Adobe servers perform a normal cookie handshake. 
* To track links, you must include pe, pev1, and pev2 parameters.

A custom link measurement URL looks similar to the following:

```
<a href=" http://johnny_appleseed.122.2o7.net/b/ss/appleseedpodcasts/4/REDIR/
?url=http%3A%2F%2Fwww.johnny_appleseed.org%2Fmpegs%2Fplanting_apple_trees.mpeg&pe=lnk_d
&pev1=http%3A%2F%2Fwww.johnny_appleseed.org%2Fmpegs%2Fplanting_apple_trees.mpeg&pev2=pl anting_apple_trees&">Planting an Apple Tree</a>
```

For more information, see the [Exit Link Tracking Redirects whitepaper](https://marketing.adobe.com/resources/help/en_US/whitepapers/redirects/). 