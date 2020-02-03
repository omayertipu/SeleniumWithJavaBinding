# SeleniumWithJavaBinding
TestProject
Import the folder into the eclipse-workspace.

The testcase:
-Opens chrome and goes to the site
-Types in "stainless work table" into the searchbar and clicks on the search button
-Goes to the last page of the search results
-Adds the last work table to cart and confirms, then goes to the cart
-Empties the cart and confirms
-Quits the browser


Created the project through Maven Project.
Need to use chromedriver 78 for the current version of chrome, it is inside src/test/resources/executables.
All the dependencies are in the pom.xml file.

Constants file, in src/main/base/wt.base, has the browser, test site, and wait time variables.

Page file, in src/main/base/wt.base, is where the browser and test site is called, also quits the browser.

All the files under wt.pages.locators have the elements of what will be interacted with on each page.
Home page where the site starts, the search result page after searching "stainless work table", 
the last result page for the last page of the tables, and the cart page where the table is emptied from.

The files under wt.pages.actions are the actions or inputs for each page and calling the locators(elements)
from the locators files respectively.
The home page sends the keys "stainless work table" to the searchbar and clicks on the search button.
The search result page clicks on the last page of tables.
The last result page clicks add the last table on the page to cart, confirms it, then goes to the cart.
The cart page clicks empty cart and confirms it.

All this is run through the testcase file, CartTest, in src/test/java/testcases.
First the Page class is called to open chrome and go to test site, then all the page actions are initilized
and the methods are called, last the Page class is called again to quit the browser.

