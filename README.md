# Jekfolio
A Jekyll site with portfolio pages and creative blogging in mind.

## What is Jekfolio?

Jekfolio is a simple, intuitive Jekyll 'theme' designed around blog posts and work pages, making it perfect for a simple portfolio site. Jekfolio runs on a static site-generating framework called Jekyll. How Jekyll works, is it compiles .md(Markdown) files that you've written into a presentable static page with your posts content; no server processes are needed for Jekyll! On top of Jekyll's helpful built-in functionalities, Jekfolio takes advantage of sass variables and mixins to create semantic and easy-to-modify code and styling for the site. Multiple different page layouts are available for use, and each post can easily specify its 'layout' template in the YAML front matter on every page.

Jekyll's speedy and efficient functionalities complimented with the modularity and progressiveness of the Jekfolio theme provide a great backbone for a portfolio page, blog, or other dynamically time-insensitive content.

## Installation

1. Ensure that Ruby and Ruby Gems are installed on your machine

2. Install Jekyll:
````
gem install jekyll
````

3. Clone the repository:
````
git clone https://github.com/Ben-Kincaid/Jekfolio.git
````

4. Open the `index.html` file in the `/_site` directory in your browser.

You're up and running! Since jekyll is a static site generator, no web server is needed for development.

## Usage

### Style Modifications
All styles are under the '_source/_sass' directory, and are imported into `_source/_css/main.scss` before being compiled to `/_site/css/main.css`. This allows for us to break our CSS/SCSS into partials, and order them in the stylesheet using ITCSS(Inverted Triangle CSS) architecture. 

ITCSS follows the thought of adding the most broad styling specifications first, and adding the most strict and specific styling specifications last. This allows us to take advantage of the global namespace of variables and mixins, along with setting element defaults and general object formatting that can easily be overriden and modified later on in the style sheet. Looking at the `main.scss` file in `_source/css` gives a documented representation of what is being added and its purpose in the stylesheet.

Most general,low-level changes you will want to make in regards to the sites styling is stored in `_scss/_tools.scss` and `_scss/_variables.scss`; these two files house the mixins, functions, and variables that dictate many general aspects of the styling of the site. 

In the variables file, there is: 
  1. Colors - these are the color variables used throughout the site; Most are labeled by color primarily, then their purpose. If they are appended with a number, that is their lightness scale: 1 is the lightest, 5 is the darkest. For example, `$grey-2` is lighter than `$grey-3`. Brand colors are names `brand-{color family}` to allow for identification that they are the main site/brand colors, yet still indicate the color range. 

