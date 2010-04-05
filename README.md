This is a native Java JSR286 portlet, that connects to a remote web app, parses its response and alters its HTML body.

Supports GET and POST, and reads cookies from the server and stores them to the PortletSession.

The Rails response is being processed by [HTML Parser](http://htmlparser.sourceforge.net/). Each HTML node is being traversed in the <head> and <body> sections. The title of the page is being set as the portlet title. JavaScripts and CSS links are being included onto the portlet's body HTML. In the body, the links and forms are transformed to PortletUrls and ActionRequests. Image URLs are also modified to take account the servlet.

