iland
=====

A cyclad-punk comic set in an alternative 1830s strand of history. 

Getting Started
---
installing
----
- Get Ruby Version Manager: `\curl -sSL https://get.rvm.io | bash -s stable`
- Get the right verions: `rvm install ruby-2.3.3`
- And use it: `rvm use ruby-2.3.3`
- Install the bundler: `gem install bundler`
- Clone the repo: `git clone https://github.com/tsouk/iland-comic.git`
- Cd in the repo dir and install the requried gems: `bundle install`
- Run the jekyll server: `bundle exec jekyll serve`

You should have a server up and running locally at <http://localhost:4000>.

Configuration
-----

The main settings happen in side of the _config.yml file:

### Site

Main settings for the site

* **title**: name of your site
* **description**: description of your site
* **logo**: small logo for the site (300x * 300x)
* **cover**: large background image on the index page

* **name**: name site owner
* **email**: mail address of the site owner
* **author**: author name
* **author_image**: small image of author (300x * 300px)
* **disqus**: add a disqus forum for your post

### Social

The template allows to add all major social platforms to your site.
Fill the the form for each platform. If you leave the share_* entries empty, the sharing buttons below a post are not shown.  If you leave the **url** and **desc** empty the icons are not shown on the index page, but the share icons on the article pages remains untouched (Thanks to [Phil](https://github.com/philsturgeon))

* **icon**:	name of social platform (must match a name of [font-awsome](http://fortawesome.github.io/Font-Awesome/) icon set )
* **url**:	url of your account
* **desc**: slogan of the platform
* **share_url**: share url
* **share_title**: first part of url for the title
* **share_link**: second part of the share url for the link to the post

The Liquid template engine will magical combine the different parts to a share url.

```
http://twitter.com/share?text=post_title&amp;url=post_url
````

See [_config.yml](https://github.com/dirkfabisch/mediator/blob/master/_config.yml) for more examples.