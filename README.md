Pointrel20140331
================

A version of the Pointrel data repository system in HTML5/CSS/JavaScript

This stores snippets of HTML entered in a text area in a local IndexedDB database in your browser. These snippets can be displayed in a list below the edit box. TiddlyWiki was a bit of an inspiration for that list display. This is intended to support "bootstrapping" more a more complex system, such as Doug Engelbart worked toward to support a co-evolution of tools, knowledge, community, and processes.

Note: Because this software uses IndexedDB, it will not currently work with Mac OS X Safari. You could try it with a diferent browser like FireFox or Chrome or try modifying the code to use a "shim" like this one: http://nparashuram.com/IndexedDBShim/  
You can check if your browser supports IndexedDB here: http://caniuse.com/indexeddb

To use this, first open the source/PointrelBootstrapLoader.html file in a web browser (which also loads require.js included in that directory). Then as a demo you can cut and paste in the contents of bootstrap/bootstrap.json into the text field and click the "Replace All" button. There are hover hints over the buttons suggesting what they can do. After you have loaded some content, you can click on "List all IDs" to get a list of all the items. Click on an item to load the content in the text area. Then click "Open view" to display that content as part of the HTML page.

After you store some content, in some web browsers you can click "Browse" to view only that content
in a new browser window instead of lower down on the editor page.
Browsed content will look like a stand-alone web page or application.
However, it is not stand-alone because it relies on the bootstrap loader.
Also, by changing "view" to "edit" in the URL parameters and reloading the page,
you can edit the content.

You can try a demo version here which will store data in your browser:  
http://rawgithub.com/pdfernhout/Pointrel20140331/master/source/PointrelBootstrapLoader.html

Here is a direct link to the bootstrap.json content to paste in as a start:  
https://raw.githubusercontent.com/pdfernhout/Pointrel20140331/master/bootstrap/bootstrap.json

Here is an alternate demo link, which will store data in a different local database associated with the different domain:  
http://htmlpreview.github.io/?https://github.com/pdfernhout/Pointrel20140331/blob/master/source/PointrelBootstrapLoader.html

"Browse" in viewOnly mode does not currently work correctly on this second site.
Also, "Browse" does not seem to work as expected with Firefox 28,
because Firefox seems to treat the query string to a file as part of the security domain -- so it creates a new IndexedDB which does not have the data.

Note:
The project's source code itself is under the MIT license.
The bootstrap.json file contains content under a mix of different FOSS licenses.
