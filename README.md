# Juunoco's Official Blog

## Creating a new Post:

Juuncoo Blog is using Jekyll and Ruby gems
In particular, it has now stopped using the default 'minima' theme, and is now using a custom theme on Github.
https://wowthemesnet.github.io/mediumish-theme-jekyll/
with documentation https://github.com/wowthemesnet/mediumish-theme-jekyll


A simple explanation has been written below, any unclarified questions can be found in the [documentation](https://jekyllrb.com/docs/usage/)

Just in case, [Here's](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) a good guide to markdown 

To include an image as a relative link:
	* put the image in the assets folder
	* link to it via markdown syntax ![image_name]({{site.url}} /image-title.png).
	* If the above doesn't work, link to the image by providing an absolute link, using http.

```
	![image-alt-name](http://juunoco.github.io/blog/assets/img/dog_meditation2.png)

```


	
===



If this is your first time on the Juunoco's blog, you will need to pull the latest git repo.
```
	git clone https://github.com/juunoco/blog.git
```

otherwise, just pull the latest repo
```
	git pull https://github.com/juunoco/blog.git
```

Create a new file under _<_posts>_ directory with the following structure
'YYYY-MM-DD-YOUR-PREFERRED-TITLE.md'

Posts will updated automatically according to listed date.	

Now, you are able to choose a few settings. This is placed in a location called the 'YAML front matter'
All you need to know is that it looks like this at the top of the document. This should always be at the start, and defines how the post will look in the page.
Please note that between this is ruby, and a space is required between the key and value e.g (layout: value) must have a space between the two, 

```
---
layout: post
title:  "What is Jekyll"
author: john
categories: [ Jekyll, tutorial ]
image: assets/images/11.jpg
featured: true
hidden: true
tags: 
cache: 
---
```

Here's a rundown of the settings.
* layout: because we are writing posts, this should be set to 'post'
* author: obvious?
* categories: if possible, please use existing categories, otherwise you can just create categories
* image: the image which features in the header, what makes the post super cool
* featured: whether this post should be placed in the 'featured' section of the blog. (probably yes, we'll have to manually trigger no, on the old ones)
*comments: should there be comments?
*hidden: if featured is true, then do not show in all posts again.


Make sure to include your name/alias at the end of the blog post, and the date of publishing in format dd/mm/YYYY.

to publish, simply push to the repo through branch "gh-pages"
```
	git add .
	git status //check for status
	git commit -m "<CLEAR COMMIT MESSAGE HERE>"
	git push origin gh-pages
``` 

###Debugging before bushing to Github and Publishing

A faster way to test content is to serve the blog live.
This has a few advantages, it will show fast debug messages. 
It's safer than live uploads
It's hotloaded, so any changes made to files and folders will be reflected live. (If nothing changes, make sure to refresh browser cache), The only exception is changes to _config.yaml. In this case, it will be necessary to press Ctrl + C, (Y) to stop execution, followed by a repeat of the command below.


You can debug live with the follwoing command
```
	$ bundle exec jekyll serve
```


Jekyll will identify and update the main site.

Make sure to check the site for finalized info.
[https://juunoco.github.io/blog/](https://juunoco.github.io/blog/)


Happy Blogging : )


## Further ToDo:

Create a press kit, maybe using pressKit();
Use MAMP to create the web server, and run install.php from presskit() from there.


### FURTHER BLOG IDEAS

Title:
How Two Students Are Starting a Games Company

About how to bring an idea into reality, and the invisible hard work behind it.
Here's some images of our early planning and initial development.

WHO WE ARE
Two students who felt a hobby for making and developing projects?
Want to show them to people, joy from seeing others on a train, etc, playing them.

About our finances...
The hours spent developing ideas, perhaps for investment, but to see how expensive it is.

-gieoon 01/02/2018
