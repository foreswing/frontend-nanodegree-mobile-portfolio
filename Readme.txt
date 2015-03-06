Ken Haulotte - Web Optimization - Project 4

Steps to Run Project:

	1. Fork Repo.
	2. Clone to local Project folder.
	3. Set up local Python3 web server - python -m http.server 8080.
	4. Set up ngrok subdomain to host project - ngrok -subdomain foreswing4 8080.
	5. Browse to ngrok.subdomain.com to initiate website.
	6. Check PageSpeed by browsing to pagespeed/insights at developers.google.com.
	7. Enter ngrok URL and Analyze to obtain PageSpeed score (92/100).
	8. Review code modifications that enhanced PageSpeed score:
		a. added asynch attr to google-analytics js file
		b. in-lined web fonts in CSS file
		c. added media attr to print.css entry
		d. in-lined all CSS into index.html
		e. scaled Pizzeria image to display size and used new version
	9. Go to Pizza page and review sources to see code modifications for resizing Pizza
		a. reduced loop iterations to "showable" pizzas - 16
		b. move as much element processing code outside of for loop as possible
		c. use console.log to determine that widths are the same for all elements
		d. use one array reference to get width thus being able to move it outside for loop
		e. use more direct element access using className vs querySelectorAll
	10. Go to Pizza page and review sources to see code modifications for obtaining FPS < 60
		a. use more direct element access using className vs querySelectorAll
		b. move as much element processing code outside of for loop as possible
		c. reduced loop iterations from 200 to "showable" pizzas - 32
		d. use translateX instead of style left to significantly improve performance
		e. use backface-visibility: hidden in CSS move class to improve performance
	11. Rinse and Repeat