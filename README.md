## Link to live version -[Studio Finish]( https://studiofinish.herokuapp.com/)

Studio Finish is an e-commerce web application that allows users to search for beauty products stored in database, add them to shopping cart and then make payment using Stripe. App has login system functionality. The guest user can browse, search, and add product to cart only. Checkout and payment option are available for registered users only.

## UX

The purpose of the project is to create an e-commerce app for everyone interested in shopping online. Layout is simple and clear. Project is accessible through all modern browsers on both desktop and mobile devices. For build the front-end functionality CSS, HTML and JavaScript is used and for back-end logic, Python with Django framework is used. As its e-commerce app payments options is available by using Stripe API.

**User Stories**

*	As a user I want easily search for product - it is achieved by using search bar available on menu bar
*	As a user I want to find more details about product - after click on selected product user is redirected to page with all details about chosen product
*	As a user I want to add product to cart - user can add product to cart and select quantity if required (1 is default value)
*	As a user I want to update / delete items from cart - user can update and delete items on cart page
*	As a user I want to pay for chosen product - after registration/login user can access checkout page
*	As a business owner I want to expand my business and increase sales
*	it is achieved by building online presence

## Layout

The layout is simple and consistent through all modern browsers. The project has been designed with a mobile first approach and it is fully responsive across devices. To achieve this Bootstrap 4 components library was used along with custom styles. Project consist following pages:
*	**Products(homepage)**

	Page where are displayed all products in form of card with image and short info about specs and price of each product

*	**Product Details**

	Page include all details about selected product - image, description, main components summary, price and add to cart button with input field allowing select product quantity

*	**Bag page / empty bag**

	Page allows to review what is in cart - Image thumbnail is displayed along with product name and possibility for user to change quantity or delete item completely. Page include total price for all product placed in cart. Below that there are two buttons, one placed on right hand side and second on the left hand side of the screen allowing user to continue shopping (left button) or go to checkout(right button). When we remove all items cart icon is displayed with short info that cart is empty, and user can go back shopping by clicking Continue 
Shopping button.

*	**Search page / no search results**

	Page displays searching results in form like homepage. There is a card with image and short info about specs and price of each product. When keyword enter search box isn't match any product, search icon is displayed along with text informing user that product is not found.

*	**Checkout page (available after user login)**

	Page like cart page but the difference is that user cannot update any product details. This is summary before payment. Page displays product thumbnail, name, quantity, price, and total price. Below that user has payment form to fill in with user details and card details. After payment user is redirected to homepage.

*	**Login**

	Page allows user to login (user get access to checkout page and payment functionality)

*	**Registration**

	Page allows user to create an account (user get access to login functionality)

**Wireframes**

*	Mobile Layout
*	Desktop Layout

## Features

The app can be accessible with or without user registration, but in that case some features will be available after registration only (checkout). Anyone is able to perform search, view results, all details about selected product, add product to cart, view and modify product on cart page.

**Existing Features**

*	search bar - allows user to search product by keyword. Return all products where search keywords appear
*	login/register system - allows user access full app functionality
*	logout
*	back to top arrow - scrolling to top of page
*	flash messages appear after user login/registration, add/update/delete and purchase product (disappears after 5s)
*	user cannot access payment page without registration/login
*	after adding product to cart small badge with product quantity appears on menu bar beside cart icon
*	Stripe payment integration
*	short product info cards on homepage
*	function preventing access restricted page(checkout) without registration/login

**Features Left to Implement**

*	add some gallery image on product details page
*	create categories (category model has been created and relation to product exist, but there are no views implemented for categories)
*	create pagination
*	create contact page
*	add confirmation email after purchase (currently only flash message appears)
*	add filters to search option (currently only search by any keyword is available)
*	customers reviews

## Technologies used

*	**Heroku** - is a platform that enables developers to build, run, and operate applications entirely in the cloud
*	**GitHub** - provides hosting for software development version control using Git.
*	**Git** - version-control system for tracking changes in source code during software development.
*	**Google Fonts** - library of free licensed fonts, an interactive web directory for browsing the library, and APIs for conveniently using the fonts via CSS ('Lato' font used in this project).
*	**Python** - programming language.
*	**JavaScript** - used to program the behavior of Web pages.
*	**jQuery** - JavaScript library designed to simplify HTML DOM tree traversal and manipulation
*	**HTML5** - standard markup language for creating Web pages.
*	**CSS3** - used to define styles for Web pages, including the design, layout and variations in display for different devices and screen sizes.
*	**VS Code** - code editor redefined and optimized for building and debugging modern web and cloud applications.
*	**Bootstrap 4** - free and open-source CSS framework directed at responsive, mobile-first front-end web development.
*	**Django** - a Python-based free and open-source web framework, which follows the model-template-view architectural pattern.
*	**Stipe** - a payment company that allows individuals and businesses to make and receive payments over the Internet


## Testing

**Automated testing**

For the testing following tools and services was used:
*	**Chrome Developer Tools** - a set web authoring and debugging tools built into Google Chrome.
*	**CSS Validation**-service helps to check validity of Cascading Style Sheets (CSS).
*	**Markup Validation** - helps check the validity of Web documents.
*	**JSLint** - a static code analysis tool used for checking if JavaScript source code complies with coding rules.
All validation tests passed: no errors in the DevTools console. CSS and JavaScript have correct syntax as well. The HTML validator did not recognise the Django template tags which resulted in showing errors.
The website was constantly tested by each time it was pushed to git. All test are passed.

**Manual testing**

Manual testing was performed by clicking every element on page which can be clicked.
1.	**Search form**
o	Available all the time on menubar
o	Try to submit empty form and verify that an error message about required fields appear - form doesn't have required attribute. After submiting returning page with all available products.
o	Try to submit the form with valid input and verify that a success message appears (after entering keyword user is redirected to results page and the product matches searching criteria are displayed)
2.	**Login form page**
o	Go to Products(homepage) page
o	Click Log in link on navigation bar (user is redirected to login page)
o	Try to submit empty form and verify that an error message about required fields appear(required field message appears)
o	Try to submit the form with valid input and verify that a success message appears (user is redirected to homepage with successful login message)
o	Try to submit the form with invalid input and verify that a error message appears (Your username or password is incorrect message appears)
3.	**Registration form page**
o	Go to Product(homepage) page
o	Click Log in link on navigation bar (user is redirected to registration page)
o	Click Create account button below the login form
o	Try to submit empty form and verify that an error message about required fields appear (required field message appears)
o	Try to submit the form with valid input and verify that a success message appears (user is redirected to homepage with success message)
o	Try to submit the form with invalid input and verify that a error message appears (Unable to register your account message appears)
o	Click Sign In under Create account button (user is redirected to login page with success message)
4.	**Add to bag form**
o	Go to Product details page
o	Try to submit empty form and verify that an error message about required fields appear (required message appears)
o	Try to submit the form with valid input and verify that a success message appears (Item added to your bag. View bag message appears)
o	Try to submit the form with invalid input and verify that a error message appears.(field has html5 type number attribute and initial default value 1 preventing entering invalid input)
5.	**bag form**
o	Go to the bag page
o	Try to submit empty form and verify that an error message about required fields appear (required message appears)
o	Try to submit the form with valid input and verify that a success message appears (bag updated message appears)
o	Try to submit the form with invalid input and verify that a error message appears (field has html5 type number attribute preventing entering invalid input and also has initial value number of the specific item, which was selected on add to cart page)
o	Click remove button - item is deleted from bag (message appears)
o	Click Shoppig button (user is redirected to products page (homepage))
o	Click Checkout button (user is redirected to checkout page)
6.	**Payment user details/ credit card form**
o	Go to Checkout page
o	Try to submit empty form and verify that an error message about required fields appear (required message appears)
o	Try to submit the form with valid input and verify that a success message appears (user is redirected to homepage and message appears)
o	Try to submit the form with invalid input and verify that a error message appears (use different card number cause error message appears)
    All fields in user details form have required attribute. Credit card forms has required attr set to false as there is some issue and payment cannot be successfully proceed.
    For Stripe payment test following details need to be used:
    Card number - 4242424242424242
    CVC - any 3 digit number
    Expiry date - any date in the future
7.	**Scrolling up and down all the pages**
o	Project was manually tested in all the major browsers including Google Chrome, Safari and Internet Explorer to confirm compatibility. The tests were conducted in virtual mode using the google developer tools and also physical mobile phones such us: Samsung Galaxy Note 9, Htc One S, Samsung A20. App looks consistent and works well on different browsers and screen sizes.
8.	**site navigation**
o	Click on Home link (redirect to index/homepage)
o	Click on logo/brand link (redirect to index/homepage)
o	Click on Log in link (redirect to login page form)
o	Click on Register link (redirect to registration page form)
o	Click on Cart link (redirect to cart page)
o	Click on Logout link (user is logged out)
o	Click on Back to top arrow icon (page is scrolling up)
All links are working and pointing to correct place.There are no dead links.
9.	**Products(homepage)**
o	Click on selected product card (user is redirected to chosen product on product details page)

## Deployment

The project was developed, committed to git and pushed to GitHub using Visual Studio Code IDE.
The project was deployed using Heroku as a hosting platform.

**Clone in GitHub**

1.	Open the e-commerce repository.
2.	Click the Clone or download button.
3.	In the clone with HTTPs pop-up, click the copy icon.
4.	Open git bash in your IDE.
5.	Change the current working directory to where you want the cloned directory to be made.
6.	Type git clone and paste the URL copied earlier.
7.	Press enter.
8.	Repository is copied.
**IDE Development Setup**

1.	Create a virtual environment for your Python project.
2.	Create a env.py file in the root project folder.
3.	Add the following variables to the env.py file:

    os.environ.setdefault['SECRET_KEY']
    os.environ.setdefault['STRIPE_PUBLISHABLE']
    os.environ.setdefault['STRIPE_SECRET']
    os.environ.setdefault['DATABASE_URL']
4.	Use pip install -r requirements.txt to install Python required modules.
For security reason the environment variables were set in a separate file env.py and are referenced by os.environ.get("KEY", "name"). Stripe account need to be set up to obtain testing keys.

**Deploy to Heroku**

1.	On the Heroku website log into your account.
2.	Click new and create new app.
3.	Give your app a name (it must be unique), select a region and click create app.
4.	Under resources choose to add on PostgreSQL hobby free.
5.	Go to settings, press Reveal vars button and copy database url.
6.	Go back to your IDE and type in pip3 install dj-database-url which will allow to connect to db url.
7.	Type pip install psycopg2 which allow connect to postgress.
8.	Type pip freeze > requirements.txt to update packages file.
9.	Fill the heroku db url value for your environment variables in the env.py file.
10.	Type python manage.py migrate to create and run migrations.
11.	Type python manage.py createsuperuser to create a super user. 
12. Return to the Heroku dashboard and under settings/ config vars click reveal vars. Add the key values for all your environment variables from env.py project file. 
13. Type pip install gunicorn - package required to connect to heroku.
14.	Type pip freeze > requirements.txt to update packages file.
15.	Create Procfile.
16.	Commit all changes to github.
17.	Go to heroku Deploy tab and in deployment method choose github connect, find you repository and press connect.
18.	Go to manual deploy and press depoy branch after while when is no error you will see url of your app.
19.	Open the Heroku app address adding /admin to the end of the URL and login with the superuser credentials.
20.	Use the Django admin interface to add data to your app.

    A live website can be found on Heroku ( https://studiofinish.herokuapp.com/)

    The repository can be found on Github (https://github.com/jayab2010/cosmetic)

## Credits

**Content**

*	The images on all the products were from [Sephora.com](https://www.sephora.com),[Jcpenny.com](https://www.jcpenney.com/)
*	The Profile Registration & Log in functions was used from the Code Institute course lesson Authentication & Authorisation
*	Parts of the design and wiring of the project was learned from the Code Institute course lesson Putting It All Together | ECommerce Mini Project

**Acknowledgements**

*	Many thanks to my mentor Usmaan Mujtaba for all suggestions and possible solutions to various issues encountered during project development process.


