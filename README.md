# Beautiful Jekyll

Check out the website: www.mattkcole.github.io

Built off a theme: [beautiful-jekyll](http://deanattali.com/beautiful-jekyll)


## Features

### Adding Google Analytics to track page views

Beautiful Jekyll lets you easily add Google Analytics to all your pages. This will let you track all sorts of information about visits to your website, such as how many times each page is viewed and where (geographically) your users come from.  To add Google Analytics, simply sign up to [Google Analytics](http://www.google.com/analytics/) to obtain your Google Tracking ID, and add this tracking ID to the `google_analytics` parameter in `_config.yml`.

### Sharing blog posts on social media

By default, all blog posts will have buttons at the bottom of the post to allow people to share the current page on Twitter/Facebook/LinkedIn.  You can choose to enable/disable specific social media websites in the `_config.yml` file. You can also turn off the social media buttons on specific blog posts using `social-share: false` in the YAML front matter.

### RSS feed

Beautiful Jekyll automatically generates a simple RSS feed of your blog posts, to allow others to subscribe to your posts.  If you want to add a link to your RSS feed in the footer of every page, find the `rss: false` line in `_config.yml` and change it to `rss: true`.

### Page types

- **post** - To write a blog post, add a markdown or HTML file in the `_posts` folder. As long as you give it YAML front matter (the two lines of three dashes), it will automatically be rendered like a blog post. Look at the existing blog post files to see examples of how to use YAML parameters in blog posts.
- **page** - Any page outside the `_posts` folder that uses YAML front matter will have a very similar style to blog posts.
- **minimal** - If you want to create a page with minimal styling (ie. without the bulky navigation bar and footer), assign `layout: minimal` to the YAML front matter.
- If you want to completely bypass the template engine and just write your own HTML page, simply omit the YAML front matter. Only do this if you know how to write HTML!

### YAML front matter parameters

These are the main parameters you can place inside a page's YAML front matter that **Beautiful Jekyll** supports.

Parameter   | Description
----------- | -----------
title       | Page or blog post title
subtitle    | Short description of page or blog post that goes under the title
bigimg      | Include a large full-width image at the top of the page.  You can either give the path to a single image, or provide a list of images to cycle through (see [my personal website](http://deanattali.com/) as an example).
comments    | If you want do add Disqus comments to a specific page, use `comments: true`. Comments are automatically enabled on blog posts; to turn comments off for a specific post, use `comments: false`. Comments only work if you set your Disqus id in the `_config.yml` file.
show-avatar | If you have an avatar configured in the `_config.yml` but you want to turn it off on a specific page, use `show-avatar: false`. If you want to turn it off by default, locate the line `show-avatar: true` in the file `_config.yml` and change the `true` to `false`; then you can selectively turn it on in specific pages using `show-avatar: true`.
image       | If you want to add a personalized image to your blog post that will show up next to the post's excerpt and on the post itself, use `image: /path/to/img`.
share-img   | If you want to specify an image to use when sharing the page on Facebook or Twitter, then provide the image's full URL here.
social-share | If you don't want to show buttons to share a blog post on social media, use `social-share: false` (this feature is turned on by default).
layout      | What type of page this is (default is `blog` for blog posts and `page` for other pages. You can use `minimal` if you don't want a header and footer)  
js          | List of local JavaScript files to include in the page (eg. `/js/mypage.js`)
ext-js      | List of external JavaScript files to include in the page (eg. `//cdnjs.cloudflare.com/ajax/libs/underscore.js/1.8.2/underscore-min.js`)
css         | List of local CSS files to include in the page
ex-css      | List of external CSS files to include in the page
googlefonts | List of Google fonts to include in the page (eg. `["Monoton", "Lobster"]`)

### Advanced features (including how to use a custom URL address for your site)

I wrote [a blog post](http://deanattali.com/2015/03/12/beautiful-jekyll-how-to-build-a-site-in-minutes/) describing some more advanced features that I used in my website that are applicable to any Jekyll site.  It describes how I used a custom URL for my site (deanattali.com instead of daattali.github.io), how to add a Google-powered search into your site, and provides a few more details about having an RSS feed.

## Creating a User Page vs a Project Page

If you're not sure what the difference is, you can probably safely ignore this section.

If you want to use this theme to host a website that will be available at `https://YOURUSERNAME.github.io`, then you do not need to read this section. That is called a User Page, you can only have one User Page in your GitHub account, and it is what you get by default when forking this project.

If you want to use this theme to create a website for a particular repository, it will be available at `https://YOURUSERNAME.github.io/REPONAME`, and that is called a [Project Page](https://help.github.com/articles/user-organization-and-project-pages/). You can have a Project Page for each repository you have on GitHub. There are two important things to note when creating a project page:

1. In the configuration file (`_config.yml`), you should set `baseurl` to be `/projectname` instead of `""`.
2. Project Pages are served from a branch named `gh-pages`, and you should be generating all the website content on that branch. When you fork Beautiful Jekyll, you'll already have a `gh-pages` branch but you should delete it and generate it again from the `master` branch. The reason is that the `gh-pages` branch in its current form does not have the updated code of Beautiful Jekyll, so you need to create that branch from the `master` branch (which is where all my new features and work go into).

## Showcased users (success stories!)

To my huge surprise, Beautiful Jekyll has been used in over 500 websites in its first 6 months alone! Here is a hand-picked selection of some websites that use Beautiful Jekyll.

Want your website featured here? [Contact me](http://deanattali.com/aboutme#contact) to let me know about your website.

### Project/company websites

| Website | Description |
| :------ |:----------- |
| [teampass.net](http://teampass.net) | Collaborative Passwords Manager |
| [derekogle.com/fishR](http://derekogle.com/fishR/) | Using R for Fisheries Analyses |
| [bigdata.juju.solutions](http://bigdata.juju.solutions) | Creating Big Data solutions Juju Solutions |
| [joecks.github.io/clipboard-actions](http://joecks.github.io/clipboard-actions/) | Clipboard Actions - an Android app |
| [embedded.guide](http://embedded.guide) | Writing an Embedded OS |
| [blabel.github.io](http://blabel.github.io) | Library for canonicalising blank node labels in RDF graphs |
| [reactionic.github.io](http://reactionic.github.io) | Create iOS and Android apps with React and Ionic |
| [ja2-stracciatella.github.io](http://ja2-stracciatella.github.io) | Jagged Alliance 2 Stracciatella |
| [PatientOutcomeFunding.org](http://www.patientoutcomefunding.org/) | Patient Outcome Funding |

### Personal websites

| Website | Who | What |
| :------ |:--- | :--- |
| [deanattali.com](http://deanattali.com) | Dean Attali | Creator of Beautiful Jekyll |
| [ouzor.github.io](http://ouzor.github.io) | Juuso Parkkinen | Data scientist |
| [derekogle.com](http://derekogle.com/) | Derek Ogle | Professor of Mathematical Sciences and Natural Resources |
| [melyanna.github.io](http://melyanna.github.io/) | Melyanna | Shows off her nice art |
| [chauff.github.io](http://chauff.github.io/) | Claudia Hauff | Professor at Delft University of Technology |
| [kootenpv.github.io](http://kootenpv.github.io/) | Pascal van Kooten | Data analytics |
| [sjackman.ca](http://sjackman.ca) | Shaun Jackman | PhD candidate in bioinformatics |
| [epwalsh.com](https://epwalsh.com) | Evan Pete Walsh | PhD candidate (Statistics and Mathematics) at Iowa State University ||
| [anudit.in](http://www.anudit.in/) | Anudit Verma | Engineering student |
| [aqibsaeed.github.io](http://aqibsaeed.github.io/) | Aaqib Saeed | Computer Science grad student |


## Advanced: Local development using Docker

Beautiful Jekyll is meant to be so simple to use that you can do it all within the browser. However, if you'd like to develop locally on your own machine, that's possible too if you're comfortable with command line. Follow these simple steps to do that with Docker:

1. Make sure that you have Docker installed on your local environment. Installation instructions can be found [here](https://docs.docker.com/engine/installation/)
2. Clone your fork `git clone git@github.com:yourusername/yourusername.github.io.git`
3. Inside your repository folder, run:

    ```
    docker run -p 4000:4000 -v `pwd`:/app mangar/jekyll:1.1 bash -c "bundle install; bundle exec jekyll serve"
    ```
4. View your website at <http://localhost:4000>.

Disclaimer: I personally am NOT using local development so I don't know much about running Jekyll locally. If you follow this route, please don't ask me questions because unfortunately I honestly won't be able to help!		

Aditionally, if you choose to deploy Jekyll using a local ruby installation, you can tell Jekyll to automatically categorize your blog posts by tags. You just need to set `link-tags: true` in `_config.yml`. Jekyll will then generate a new page for each unique tag which lists all of the posts that belong to that tag.


## Credits

This template was not made entirely from scratch. I would like to give special thanks to:
- [Barry Clark](https://github.com/barryclark) and his project [Jekyll Now](https://github.com/barryclark/jekyll-now), from whom I've taken several ideas and code snippets, as well as some documenation tips.
- [Iron Summit Media](https://github.com/IronSummitMedia) and their project [Bootstrap Clean Blog](https://github.com/IronSummitMedia/startbootstrap-clean-blog), from which I've used some design ideas and some of the templating code for posts and pagination.

I'd also like to thank [Dr. Jekyll's Themes](http://drjekyllthemes.github.io/), [Jekyll Themes](http://jekyllthemes.org/), and another [Jekyll Themes](http://jekyllrc.github.io/jekyllthemes/) for featuring Beautiful Jekyll in their Jekyll theme directories.

## Contributions

If you find anything wrong or would like to contribute in any way, feel free to create a pull request/open an issue/send me a message.  Any comments are welcome!

Thank you to [all contributors](https://github.com/daattali/beautiful-jekyll/graphs/contributors). Special thanks to the following people with non-trivial contributions (in chronological order): [@hristoyankov](https://github.com/hristoyankov), [@jamesonzimmer](https://github.com/jamesonzimmer), [@XNerv](https://github.com/XNerv), [@epwalsh](https://github.com/epwalsh), [@rtlee9](https://github.com/rtlee9).

If you do fork or clone this project to use as a template for your site, I would appreciate if you keep the link in the footer to this project.  I've noticed that several people who forked this repo removed the attribution and I would prefer to get the recognition if you do use this :)

## Known limitations

- If you have a project page and you want a custom 404 page, you must have a custom domain.  See https://help.github.com/articles/custom-404-pages/.  This means that if you have a regular User Page you can use the 404 page from this theme, but if it's a website for a specific repository, the 404 page will not be used.
