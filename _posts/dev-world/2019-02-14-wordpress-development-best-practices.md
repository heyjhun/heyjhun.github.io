---
layout: post
title: "Wordpress Development Best Practices"
author: "HeyJhun"
categories: web-dev-world
description: In a Wordpress Event held in Ortigas, one Wordpress Developer veteran shared his best practices for newbies like us. He also shared some common errors that we may encounter and how to deal with it.
tags: [documentation,sample]
image: wordpress-development-best-practices.jpg
---

## Some of the Best Practices in Wordpress Development

I recently attended a Wordpress Event held somewhere in Ortigas. 

Some of the key takeaways which I somehow managed to remember are the following:

1. Use an IDE or text editor designed for development: VSCode, Atom, Brackets

2. Do not modify core WP files, plugin, and parent theme.

3. Use grunt or gulp to aggregate JS and CSS on your local development environment.

4. Use linter or put it in your build server.

5. Leverage CDN, Leverage caching

6. Dev Environment > Test > Live

7. SDLC (Software Development Life Cycle)

8. Do not just rely in installing plugins if you want to become a full stack Wordpress Developer.

These are just basic rules or good practices that I remember which I think would make sense when working as a Wordpress Developer. 

## Handling Common Errors

The speaker also shared some knowledge regarding the common errors that a Wordpress Developers encounter and how to fix them.

Here are some of it:

- Whitescreen of Death
	* Increase memory limit
	* Disabling the last plugin used
	* Replace the theme with the default theme

- Internal Server Error
	* Check the corrupt .htaccess file
	* Increase memory limit
	* Disable plugins
	* Reupload core files
	* Contact the hosting provider

- Database connection error
	* PHP Version used not compatible with the database
	* Database might be corrupted
	* Credentials

If you want to dig more some of the best practices for Wordpress development, the speaker also left us a reference where we can find something useful. Just search on Google: Coding Standards Wordpress.