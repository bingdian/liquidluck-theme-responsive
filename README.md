# liquidluck-theme-responsive Theme for Felix Felicis

## Installation

Requires Felix Felicis 3.8+

### Install

Git clone this repo, and place it in your blog:

	git clone https://github.com/lepture/liquidluck-theme-responsive.git _themes/responsive

	your_blog/
    	settings.py
    	content/
    	_themes/
       		responsive/

## Configuration

Edit your settings, change your theme to ``responsive``.


## Customize

You can customize your theme with ``theme.vars``.

Change Navigation (example)

	theme = {
		'vars': [
			'nav': [
				{'name': 'Home', 'link': '/'},
				{'name': 'Life', 'link': '/life/'},
			]
		]
	}

Google Analytics

	theme = {
		'vars': {
			'analytics': 'UA-xxxx',
		}
	}

Disqus Comment Support

	theme = {
		'vars': {
			'disqus': 'your-disqus-shortname',
		}
	}

## 404

You can create a file in your source directory (``content``) named ``404.md``.

	# 404
	
	- template: 404.html
	
	----------------

	You content here.

Configure your nginx, add:

	error_page 404 /404.html;


## Allow comment

If you post is not public, this post will not be allowed to comment.
If you want to allow people to comment on your secret post, set

	theme = {
		'vars': {
			'allow_comment_on_secret_post': True
		}
	}

## Write a Review

This theme supports [review microdata](http://support.google.com/webmasters/bin/answer.py?hl=en&answer=146645#Individual_reviews).

Write your post:

	# title
	
	- date: 2012-12-12
	- review: movie or book title
	- rating: 4
	
	------------

	content

Rating is optional, the max rating is 5.
