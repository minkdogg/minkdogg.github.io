## Website Performance Optimization portfolio project

####Run Instructions

To evaluate project for part 1, open index.html in a web-browser (Chrome preferred).

To evaluate project for part 2, open pizza.html found in folder 'views'.

####Project Notes

Another great project. I included my non-minified index.html file in case you wanted to look it over. Nothing special, but I just included it for reference.

The PageSpeed Insights score I received for index.html were 95 for mobile and 97 for desktop with browser cashing as the suggestion for improvement.

Feel free to ask any questions. Very interesting topic and something I should continue to investigate (especially improving frame rate optimization). Part 2 wasn't my best work, but I believe it was optimized enough to complete the project.

To minify my index.html file, I used the following link:
http://www.willpeavy.com/minifier/

To compress my images, I used jpegtran
http://jpegclub.org/jpegtran/


####Part 1: Optimize PageSpeed Insights score for index.html

    1) Moved the google analystics internal scripts to the bottom of the page as they were not needed in the beginning espcially since they were not needed to display html.

    2) Added "async" to all additional scripts (analystics.js, perfmatters.js, and the webfont internal script)

    3) Added media="print" to css link for print.css so stylesheet isn't blocking on initial load.

    4) Moved all styles to an internal style sheet rather than external as the stylesheet wasn't very long. I went back and forth on this as this sheet is used for other documents, but felt like the internal stylesheet would work for the front page.

	5) I used the webfont loader from google to assist in making the custom font download without it being render blocking.

	https://developers.google.com/fonts/docs/webfont_loader?hl=en
	6) I compressed the pizzeria.jpeg image and the profilepic.jpeg image using jpegtran.

	7) Minified index.html by using the link above.


####Part 2: Optimize Frames per Second in pizza.html

	*New for Submittal 2*
	1) (Starting at Line 453) To acheive a time of less than 5ms to resize pizza, I added a new array called pizzaSizeContainers to contain all elements with the class name randomPizzaContainer. I moved dx and newwidth outside of for loop so these values would not be recalculated during each iteration.

	2) (Starting at Line 512) Added variable 'topLocation' to calculate value once. Probably not needed for this task, but I did it in case I used the value again.

	3) (Starting at Line 519) Instead of using querySelectorAll, replaced with getElementsByClassName to improve performance of retrieving items.

    4) (Starting at Line 519) Moved 'items' array outside of for loop to avoid layout thrashing!

    *New for Submittal 2*
    5) (Starting at LIne 525) Based on great project review advice, created an additional for loop to store the 5 phase values in an array, instead of re-calculating the same 5 values over and over again.

	*New for Submittal 2*
	6) (Starting at Line 556) Changed the number of pizzas generated to a dynamic number based on the screen height. The number of pizzas generated was excessive because most of the pizzas were not shown.
    


