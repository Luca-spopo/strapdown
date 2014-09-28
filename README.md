# Strapdown+Navigation

Strapdown creates Markdown documents using Bootstrap/Bootswatch themes. No server-side compilation is required. 

For an example see http://strapdownjs.com

This project modifies Strapdown and adds a top Navigation menu to the documents.

For an example see [Strapdown+Navigation](http://smzg.github.io/strapdown/example)  

One can use this example as a template.  
Parameters should be defined in a meta tag with id='page-params'.
Possible parameters are

* theme - Name of a bootswatch theme, default is spacelab
* title - Title written in the navbar. If empty, the title of html document is used
* menu -  menu string of the form 'Name 1, Link 1, Name 2, Link 2, ...'
* active - number of the active menu item
* root - path added to the links in the menu string, default is "".

Markdown text should be inserted inside xmp or textarea tags.  
Several such tags can be used (only xmp or only textarea).  
They can have attribute cols (1 to 12, default is 12) for a narrow text column. 


###Example

```html
<!DOCTYPE html>
<html> 
<head>
<title>Example</title>
<meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
<meta id='page-params'
	theme='spacelab'
	title='Strapdown+Navigation'
	menu='Home,index.html,Menu 1,menu1.html,Menu 2,menu2.html,Menu 3,menu3.html' 
	active='1'
	root=''>
</head>

<body style="display:none">

<xmp>
#Home

* Markdown text
</xmp>

<script src="config/strapdown.js"></script>
</body>
</html>
```

###Changes
* Bootswatch themes 3.2.0 are used https://github.com/thomaspark/bootswatch
* strapdown.js containes minimized version of
	* jquery.js http://jquery.org
	* bootrsrap.js http://getbootstrap.com
	* marked.js https://github.com/chjj/marked
	* Google code prettify https://code.google.com/p/google-code-prettify/
* Several xmp/textarea tags can be used
* Parameters are saved in ``<meta id='page-params' theme=...>``