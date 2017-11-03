---
layout: post
title: Using Jekyll with Hyde
---

Hi, this is a blog about me using Jekyll!

### Using Jekyll

Here's what I think about Jekyll:

* Adding new pages and content is pretty easy, since Markdown is more intuitive than using HTML although not quite as simple as adding new pages and posts using a dynamic CMS like Wordpress
* One of the annoying things that would trouble laymen is the need to use terminal and command line often, something that would be scary for anyone not a developer.
* Customising themes is about as hard as it is for Wordpress, maybe slightly harder.


### Installation

* Installation of Jekyll was difficult at first since it required Ruby to be updated along with Ruby Gems. Doing so on Mac OSX was tricky but once that was finished Jekyll was much easier to install. See the installation guide [here](https://jekyllrb.com/docs/installation/).
* Also this easy-to-follow guide touches on Installation of Jekyll as well as the rest of setting up a Jekyll website using the Hyde theme.
*Assuming that all pre-requisite system requirements are installed, just go to terminal and type:  
`$ gem install jekyll`


### Setting up the website
* Creating a new website with the default Jekyll settings is the next step. I ran the website on my desktop like so:  
`$ cd Desktop/`  
`$ jekyll new portfolio`

* Now go into the folder of the new website in the terminal and run the website on a local server like so:  
`cd portfolio/`  
`jekyll serve`  

* Open localhost:4000 in the browser and it should appear like this:
![screenshot](/assets/Screenshot 2017-11-01 19.41.19.png "Screenshot of vanilla Jekyll website")

### Adding Hyde

* The website's appearance is a little underwhelming. Let's add one of the more popular themes, Hyde (Get it? Jekyll and Hyde?) to the website to spice it up

* Since we haven't made any content in the portfolio website, we can just ditch it. In the terminal, just go 'control -c' to stop the website being run in the server

* Download the theme, just go to https://github.com/poole/hyde and download the .zip file
* Unzip the file, move the folder 'hyde-master' to the desktop
* Go into the folder in Terminal 

* Use the `jekyll serve` command.
* If there are any errors, it is likely due to Hyde being built on an older version of Jekyll that's no longer compatible. If that's the case then just find the _config.yml file within the folder and change the settings to these:
![screenshot](/assets/Screenshot 2017-11-02 09.01.28.png "Screenshot of current settings")

* The settings should now work, use `jekyll serve` again, then go to localhost:4000.

* The website should now look like this:
![screenshot](/assets/Screenshot 2017-11-01 20.29.11.png "Screenshot of current settings")

### Customising the website
* The theme can be further edited to change the colours, by changing the class of the body in /_layouts/default.html
* See the different 8 different theme colours available:
![Hyde theme classes](https://f.cloud.github.com/assets/98681/1817044/e5b0ec06-6f68-11e3-83d7-acd1942797a1.png)

* This website uses `.theme-base-0d`

* The website layout can also be reversed by adding "layout-reverse" class to the 'body' element in default.html

* Any further editing appearance-wise can be done by editing the 'hyde.css' and 'poole.css' files. Keep in mind that the Hyde theme is built on top of the Poole theme, so both will have to be edited. They can be found by going to /hyde-master/public/css

* Editing the structure of the website by coding over the head.html and sidebar.html files in the '_includes' folder and the default.html, page.html, and post.html files in the _layouts folder

* You should never touch the '_site' folder as is simply the final product of Jekyll compiling and rendering all the other files and folders outside the folder. Any inconsistency between files in the _site folder and the rest of the files outside the folder could risk breaking the website!

* Posts are kept in the '_posts' folder. Simply copy one of the example posts as a template and start editing to add new content to the website.

### Cross-browser

This website was tested using Google Chrome, Safari, and Opera. There were no difference to be noted across the three sites.

Thanks for reading my blog post!
