iland
=====

A cyclad-punk comic set in an alternative 1830s strand of history. 

Getting Started
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
```

See [_config.yml](https://github.com/dirkfabisch/mediator/blob/master/_config.yml) for more examples.

Sketchbook
----------

Download a set of images in jpg formata and put them in a separate folder in your worskspace.
Rename all image files, starting from the latest number active +1 (eg. 00024.jpg -> 25), by using the following line in the folder with the image files. For latest number `25`:
```
a=25; for i in *.jpg; do new=$(printf "%04d.jpg" "$a"); mv -i -- "$i" "$new"; let a=a+1; done
```
We use 20% size 80% JPEG quality thumbs for fatser loads. To make these you need the imagemagick library installed and then to run the following command from the `assets/sketchbook_files` directory:
```
mogrify -resize 20% -format jpg -quality 80 -path ../sketchbook_thumbs *.jpg
```

Fonts
-----
website + title scenes:  https://fonts.google.com/specimen/Libre+Baskerville?selection.family=Libre+Baskerville

Final Cut
---------
File are put into directories by chapter number and title
```
├── 0_clouds
   ├── 0_clouds_pageXX
   ├── gr_0_clouds_pageXX
   ├── bw_0_clouds_pageXX
   ├── gr_bw_0_clouds_pageXX
   ├── web_0_clouds_pageXX
   ├── gr_web_0_clouds_pageXX
```

# Helpful scripts
### Crop all JPEGs in a folder (imagemagick)
```
for i in *.jpg; do convert $i -gravity Center -crop 1152x1691+0+0 converted_$i; done
```

Copyright
---------
Copyright of work comes by [default in the UK](https://www.gov.uk/copyright/overview)