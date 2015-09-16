## Website Performance Optimization portfolio project

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

	1) (Starting at Line 505) Added variable 'topLocation' to calculate value once.

	2) (Starting at Line 510) Instead of using querySelectorAll, replaced with getElementsByClassName to improve performance of retrieving items.

    3) (Starting at Line 510) Moved 'items' array outside of for loop to avoid layout thrashing!

	4) (Starting at Line 538) Changed the number of pizzas generated (i) to 32 (was 200) to account for max screen size of 1024 x 2048. The number of pizzas generated was excessive because most of the pizzas were not shown.
    


