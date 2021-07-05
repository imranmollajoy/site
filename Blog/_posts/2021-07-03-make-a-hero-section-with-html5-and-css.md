---
layout: post
title: Make a hero section with HTML5 and CSS
category: Web Development
tags: hero section with HTML5 and CSS, make a hero section, what is a hero section
tag:
  - make a hero section
  - hero section
  - hero section html css
date: 2021-07-01T12:28:21.235Z
img: /img/uploads/wastenot-landing-page.jpg
---
## What's a hero section

A hero section or hero image is the top element of a webpage that is full-width and sometimes full height of device screen. It may contain an full-sized image, video or animation in background and a big text. Sometimes it has call-to-action button. 

## Why a hero section

Hero section is cool. It is essential for modern website design. A hero section gives a website nice personality and look. The first thing visitor will notice is the hero section. It creates a positive feelings for them.

## Lets make one

Making a hero section is super easy. For this tutorial, we will use an image for our hero section's background. You can use a video too if you want to. 

Firstly we will create two files named index.html and style.css in a same folder. Also bring the image you want to use in that folder. In my case, the image name is header-img.jpg

Then open index.html in your favorite text editor and add the basic html markup as following: 

```html5
<!doctype html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<!-- Setup the viewport for consistent view -->
	<meta name="viewport" content="width=device-width, initial-scale=1">
	<!-- Include the stylesheet -->
	<link rel="stylesheet" href="style.css">
	<title>Hero Section</title>
</head>
<body>
	
</body>
</html>
```

Next in the body, we will create a section with an id named hero.

```html5
<section id="hero">
</section>
```

Then add the following code inside the section:

```html5
<h3>Hero Section is Awesome</h3>
<a class="cta">Yup!</a>
```

Now your code should look like this:

```html
<!doctype html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<meta name="viewport" content="width=device-width, initial-scale=1">
	<title>Hero Section</title>
</head>
<body>
    <!-- The hero section -->
	<section id="hero">
	   <h3>Hero Section is Awesome</h3>
       <a href="#" class="cta">Yup!</a>
    </section>
</body>
</html>
```

Now open the index.html in your browser. Doesn't look great, right? Let's fix this.
It's time for the styling! Open style.css and add this. 

```css
body{
    margin: 0;
}
h1{
    font-size: 4em;
    font-weight: 800;
    color:rgb(253, 255, 126);
    /* Bring the call to action closer */
	margin-bottom: 16px;
}
```

Next style the call to action. Add following code:

```css
a.cta{
    background: rgb(0, 255, 170);
    padding: 16px 64px;
    border-radius: 8px;
    font-size: 1.7em;
    text-decoration: none;
    color: rgb(34, 32, 26);
    
}
```

So far so great. But we are not done yet. Now we will style the main thing, the hero section.
Add this code in style.css:

```css
section#hero{

    /* Make the section full width */
    width: 100%;
	/* Make the section 80% of viewort height  */
    height: 80vh;

	/* The hero image and a linear gradient to add an overlay */
    background: linear-gradient(rgba(0,0,0,0.6) 60%, rgba(255, 255, 255,1)), url("header-img.jpg");
	/* Do not repeat the image */
    background-repeat: no-repeat;
	/*make the image to resize according to viewport */
    background-size: cover;
}
```

Refresh the browser. Yayy! You made a cool hero section. But the heading and the call to action is not positioned nicely. Let's work on that. Insert this code inside section#hero.

```css
    display: flex;
    /* Center elements horizontally */
    justify-content: center;
    /* Center elements vertically */
    align-items: center;
    /* Elements will stack on top of each other */
    flex-flow: column;
    /* Make the text align on center */
    text-align: center;
```

style.css should look like this:

```css
   body{
    margin: 0;
}
h1{
    font-size: 4em;
    font-weight: 800;
    color:rgb(253, 255, 126);
    margin-bottom: 16px;
}
a.cta{
    background: rgb(0, 255, 170);
    padding: 16px 64px;
    border-radius: 8px;
    font-size: 1.7em;
    text-decoration: none;
    color: rgb(34, 32, 26);
    
}

section#hero{

    width: 100%;
    height: 80vh;
    background: linear-gradient(rgba(0,0,0,0.6) 60%, rgba(255, 255, 255,1)), url("header-img.jpg");
    background-repeat: no-repeat;
    background-size: cover;

    display: flex;
    justify-content: center;
    align-items: center;
    flex-flow: column;
    text-align: center;
}
```

That's it. You've made a cool looking hero section for your website that'll draw visitors attention.

### Make sure

 Don't use any image/video that is large in size,