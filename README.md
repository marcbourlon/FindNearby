I installed the "managed package"... what now?
=====
You will not find any of the files in your Salesforce instance if you installed this app from the AppExchange. You will need to uninstall the managed app, download this entire project, and use the Force.com IDE to deploy the files to your sandbox, then test (hopefully you get your 75% code coverage), and finally deploy to you production SalesForce.com website. Here is some documentation from SFDC (SalesForce Dot Com): http://wiki.developerforce.com/page/Deploy_Force.com_Applications_Faster


HOW TO UPDATE / INSTALL:
=====

As of 11/27/2013, there is only 1 page to update.

1. Login to your salesforce instance.
2. Goto the top right and hover your name, then choose setup.
3. In the search on the left type "pages" and select Develop->Pages.
4. Find the VisualForce page called "FindNearby" and click edit.
5. Come back to this GitHub Repository and navigate to the same page:
https://github.com/scarstens/FindNearby/blob/master/src/pages/FindNearbyMap.page
6. Copy the contents from GitHub, got back to VisualForce and erase the contents, 
then paste the contents from GitHub as a replacement.
7. Save the VisualForce page and test by selecting the "Map It" link on a contact or lead.


![Screenshot from FishFinder](http://scarstens.github.io/FindNearby/images/aa_fishfinder_1.0.1_sample.png)

UPDATE REVISION NOTES
=========
Note that this version of the app has been code named FishFinder. You will know you are using the correct version 
when you see title FishFinder X.X.X as a version number at the top of your FindNearby page.

Version 1.0.1
- Fixed API key to use GKEY from the custom FindNearby Options page.
- Adjusted right lists to work when company name breaks to 2 lines.
- Adjusted borders to look correct
- Added HTML5 verticle span "button" that identifies pin type when pins are clicked (and color matches 
pin to associate purple with CONTACTS)
- Fixed double click to "add to route" and applied it to the pins as well, you may now double click pins to add them to the route.
- Double clicking pin or list item now also "removes" it from the route, if it its already in the route.

Version 0.9.3
- Upgraded jQuery and jQueryUI to most current version available
- **FEATURED** Upgraded Google Maps to V3 and rebuilt entire javascript code base to work with new API.
- Seperated javascript from VisualForce componenets to simplify the VF page, JS library file currently hosted at api.raprec.com
- Removed "Street View" option from the product, as the API calls to use this product require $10,000 API license.
