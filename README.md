#Customized Bootstrap 3 for Training Slate

##Install

In root of project:

    bower install
    npm install
    
Do a test build:

    gulp
    
If it fails bitching about lib-sass or similar bullshit, do:

    npm install --save-dev gulp-sass@2
    
Gulp again, you should be good to go.

## How it Works

`gulpfile.js` controls the flow of compilation. In there, you'll see it
grabs the `css/trainingslate.scss` file as its source. That file, in turn, 
imports `css/trainingslate_variables.css`. The variables file is where you 
override the default values for stock Booty. The initial example has a 
ton of shit overloaded, but sometimes all you need are the colors.

The `css/trainingslate.scss` basically imports, in order, the variable overloads, 
regular Booty source, any Theme, then attaches the rest of the shit in the
file. This file is good place for global overloads (like completely
changing buttons as in this example).

##Output

Finished goods are in `public/`.

##Try It

In PHPStorm, right clock on `index.html` and Run it. This is a simple
test page using the new bootstrap.