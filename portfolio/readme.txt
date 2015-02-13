Read Me File for Project 4 - Website Optimization
=======================================================

PageSpeed/Portfolio optimization (part 1):

URL for PageSpeed test: http://pnellesen.github.io/portfolio/index.html

Optimizations - Minified and inlined the CSS and Javascript, resized and optimized pizzeria.jpg, and resized/optimized profilepic.png

Result: PageSpeed scores for mobile were 96/100, and for desktop were 97/100

Information sources: mainly used the information presented in the videos, along with checking out some of the documentation at the Google Developers site pertaining to Performance Optimization (https://developers.google.com/web/fundamentals/performance/)

------------------------------------------------------------------------

Improving animation/FPS (Part 2):

URL: http://pnellesen.github.io/portfolio/views/pizza.html

This url makes calls to minified versions of the improved Javascript. The unmimified (and commented) JS can be found at http://pnellesen.github.io/portfolio/view/js/main.js

Major improvements made:

1. Completely rewrote the "changePizzaSizes" function to move almost all calculations against the pizza DOM elements outside the loop. Since all pizza elements are the same size, we only need to calculate the new sizes and DX values for the first one, recalculate the width, then apply the new width value to the other pizza elements in the collection.
2. Created "global" variables for "items" collection, along with a variable to store the length of the collection. Set the items collection during processing of the DOMContentLoaded event (at bottom of file) then used these objects in the "updatePositions()" function, rather than calculate them each time updatePositions() is called.

Other optimizations included resizing/optimizing pizza image, as well as minifying the CSS and Javascript.

Results: 

1. Pizza resize times recorded in console are consistently around the 1ms mark (sometimes slightly higher, sometimes slightly lower).
2. Average times to generate 10 frames consistently recorded in console between 1ms and .4ms (depending on browser and computer used).

Information sources: There was very little information provided in the class for tips/trick to optimizing FPS. My main source of information was posts in the forums from other students, as well as tips from the instructors to questions I posted.
