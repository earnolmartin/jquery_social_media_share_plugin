# Simple Social Media Sharing
jQuery Social Media Sharing Plugin

### About

Simple Social Media Sharing is a jQuery plugin that allows you to quickly transform an existing div element into a fully functional social media sharing widget.

### Usage:
1. Make sure the jQuery library is loaded in the <head> section of your web page.
2. Include the simple_social_share.min.js and simple_social_share.min.css files after loading the jQuery library like so:
```
<head>
	<script type="text/javascript" src="https://code.jquery.com/jquery-1.12.3.min.js"></script>
	<script type="text/javascript" src="simple_social_share.js"></script>
	<link rel="stylesheet" type="text/css" href="simple_social_share.css">
	<title>Page Title</title>
```
3. In another script, within the document.ready jQuery function, use a jQuery selector to specify which element you want to change into a social sharing widget by calling the .simpleSocialShare function.  Here's an example:
```
<script type="text/javascript">
	$( document ).ready(function() {
		$("div.shareThis").simpleSocialShare();
	});
</script>
```
4. Make sure your div element that you are transforming into a sharing widget exists in the body.
```
<body>
	<div class="shareThis"></div>
</body>
```
### Options:

- url:  The page URL to share (defaults to the current page URL if none is specified).
- title:  A short title for the content being shared (defaults to the current page title if none is specified).
- description:  Description of the content being shared (defaults to the current page meta tag description if none is specified).
- image:  Image URL for the content being shared (this setting rarely applies to any social networking sites... by default, Facebook and Twitter use these meta tag properties):
```
<meta content="https://www.google.com/images/branding/googlelogo/2x/googlelogo_color_272x92dp.png" property="og:image">
<meta content="https://www.google.com/images/branding/googlelogo/2x/googlelogo_color_272x92dp.png" property="twitter:image">
```
- sites:  Specify which social media sites are included in the sharing widget IN ORDER separated by commas (defaults to all - leave the setting empty or blank to use all supported social media sharing sites)
  - values:
    - facebook
    - twitter
    - google
    - linkedin
    - pinterest
    - email
    - whatsapp (shows only if a mobile device is detected)
    - reddit
  - examples:
	- just facebook, twitter, and email:  sites: "facebook,twitter,email"
- orientation: horizontal or vertical for the button / social media buttons layout.
- shareType: 
  - values:
    - text: Show "Share on:" text before social media buttons (Does not show if orientation is set to vertical)
    - button: A toggleable button for showing / hiding your specified social media sharing networks
    - none: Shows nothing but the social media sharing buttons
- triggerButtonActiveState: true or false boolean... if true, the button will be in a clicked state on initialization showing all of the social media buttons
- buttonSide: left or right - Only works with shareType of button... places the share button on the left or right side of the social media icons
- facebookAppId: Your Facebook App Id to customize sharing better on Facebook (default is none).
  
### Return Methods:
none

### Practical Examples:
```
<script type="text/javascript">
	$( document ).ready(function() {
		// Horizontal layout with toggle button
		$("div.shareThis").simpleSocialShare({sites: "email,facebook,google", url: "http://www.google.com", title: "Google", description: "Father of the Internet", image: "https://www.google.com/images/branding/googlelogo/2x/googlelogo_color_272x92dp.png", shareType: "button", triggerButtonActiveState: true, buttonSide: "left", orientation: "horizontal"});
		
		// For vertical with no button or text specifying sharing
		$("div.shareThis").simpleSocialShare({sites: "twitter,google,facebook", url: "http://www.google.com", title: "Google", description: "Father of the Internet", image: "https://www.google.com/images/branding/googlelogo/2x/googlelogo_color_272x92dp.png", shareType: "none", buttonSide: "right", orientation: "vertical"});
	});
</script>
```

### Supported Browsers:
- IE 9-11+
- Edge
- Firefox
- Chrome
- Safari

### Screenshot:
![Alt text](simpleSocialShare.png?raw=true "Social Media Sharing Plugin Screenshot")
