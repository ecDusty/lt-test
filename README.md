# Web Developers Starting Tool Kit

Welcome to _ecDusty's_ site off of a provided Mock Up.

## Difficulties Encountered

	1. Matching the Site to the layout as closely as possible.
		* The best option to ensure that the site I produced matched the provided PSD layout was bad saving the layout as a jpeg, then having it load in an absolute position in the body and finally applying an opacity of between 0.2-0.4 while I built the site.
		* This allowed me to observe how close I was getting the final site to the layout.

	2. Font: I didn't have available the OpenSans font, on my PC or for the Website.
		* To get around this I used my typekit acount to get the OpenSans font for the PC, then created a font kit for the website, so can also have access to the required font.

	3. Banner: Took too long to build the banner completely in HTML & CSS
		* It seems the banner was created through many different layers on Photoshop. I originally wanted to make the banner on the site through HTML & CSS and use the curtain as it's background.
		* Considering the amount of time this would take, it was much quicker to convert the banner to an image, and have the image react responsively to the screen size.

	4. Footer Background: Difficulty finding the perfect match to the gradient background.
		* To save time I saved the footers background as a png and had it load as a background image

	5. Problem remember all necessary CSS syntax.
		* When ever there there was any CSS property I was using and couldn't remember the information required to use it, I refer to either https://developer.mozilla.org/en-US/docs/Web/CSS/Reference or csstricks.com to ensure they are used correctly.




## Folder Layout

As you can see there is just the 1 folder within this repository:
	* _src_: Contains the source code of your website. Basically the easy to read and edit version of the site.

When you have gulp up & running and are testing/ distributing your site, you'll see 2 more folders being created during this process:
	* _test_: This is the folder which will hold the code that is still under testing.
	*_dist_: This is the distribution code of my site. All the code here is just the minified versions of the source code.


## Creating Distribution Ready Code From Your Source Code

Once you've tweeked your source code to your liking, its  time to minify your HTML, CSS and JS. Also lets not forgot about optimizing your images as well! Don't just minify your source code files! This is very important to leave your source code files in form that is easily readable and editable, should they require tweeking in the future.

The best way to produce your distribution ready site is to use a tool like gulp or grunt which automates this process. The amount of time saved compared to the amount time needed to learn gulp or grunt is exponecially huge!

Pick which ever tool you find works best for you, but for this toolkit _Gulp_ is used.

### Getting started up Gulp.

As I develope on a Windows machine, these instructions are for windows users, but for the most part I believe they should work on Mac's as well as I use Git's Bash command line (Instead of PowerShell).

1. Install npm on your machine
		* The simplest way of doing this is installing [Node JS], found at the provided link.

2. Install Gulp Globally - _using command line_
		* Make sure to include the '-g' flag. This tells npm to install it globally.
		```sh
		$ npm install gulp -g
		```

3. Run npm install program - _using command line_
	* As you have already downloaded my project, you have my **package.json** file, which has a list of all the dependencies and devdependencies needed for the project. By running 'npm install', your tell npm to run it's 'install' package on all the dependencies & devdependencies located within the package.json file.
	* This is quicker than installing each gulp package required seperately
		_* Make sure your are in the repository folder before you start the npm install process_
		```sh
		$ npm install
		```
			*Small side note, gulp-eslint doesn't always install correctly. You may have to install it a second time to make sure.
			```sh
			$npm install gulp-eslint
			```

4. Start testing your website
	* Just run gulp. This will create the test version of your site within the created 'test' folder and start a local server.
	```sh
	$ gulp
	```

	a. Run your local server for testing
	* Using 'gulp serve:dev' you can launch the website. **Serve** will watch to see if any changes are made to the source files, create the testing version of those file, than update the browser for you.
	```sh
	$ gulp serve:dev
	```
	* Should you like to make any changes to the site and make it your own, just start editing the files within the 'src' folder, **Serve** will handle the rest.

5. Run your Production ready Site
	* You're finished editing the site to your liking, give it one last test and run the 'serve:dist' task. This will export you project to the 'dist' folder while also creating the smallest version of each file.
	```sh
	$ gulp serve:dist
	```

6. Export your production ready project
	* This will fill your 'dist' folder with your production ready code, then zip up both the 'src' & 'dist' folders. Giving you one file to send off.
	```sh
	$ gulp export
	```


## The TO-DO List


[GO-CSS]: <https://developers.google.com/speed/docs/insights/OptimizeCSSDelivery> "Google's Optimized CSS Delivery"
[GitHub Pages]: <https://pages.github.com/> "GitHub hosting solution GitHub Pages"
[Node JS]: <https://nodejs.org/en/> "Node.JS's main page"
