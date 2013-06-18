# Level Up Sass Style Guide
*By Scott Tolinski*

#### Philosophy
The Level Up Style Guide exists to aid in clean, readable, and organized sass/css. This is not intended to be groudbreaking, just a collection of organization techniques borrowed from many other style guides. These guides can be found at the bottom of this readme.

#### File Structure
Files are organized into two folders

- sass/
- css/

The contents of these folders should be pretty straight forward. The sass folder contains partials, and sass files and will compile into the css folder with the included compass config.rb file. Partials include:

- _base.scss
- _mixins.scss
- _normalize.scss
- _vars.scss

_base.scss imports all partials as well as Compass so that _base.scss is the only partail required to import into main.scss

	@import 'compass';
	@import 'normalize';
	@import 'vars';
	@import 'mixins';

#### Table Of Contents
The Table Of Contents may be proceeded with a ascii art depending on the appropriateness of the situation. For personal projects and non-professional clients.

    /*------------------------------------*\
        $TABLE OF CONTENTS
    \*------------------------------------*/
    
    /**
     * BASE...................Brings in Compass, Normalize, Susy, Variables and Mixins
     * Main Section...........Main Section of CSS
     * Main Section...........Page Content
     * * Content Section......Content Section #1
     * * * Content Sub-section
     */
Base is the first item, the descriptor text gives a brief description of what you can find there. From there you would add main sections of your css. In the example below, notice how the main sections are things like Utilities, Element Base Styles, Content. Next we have Content Sections which more or less define section specific styles. Things like header and footer, nav are appropriate here. For this example the site is a one pager, so we have sub-sections for the main content. These can be thought of as page-specific styles.

    /**
     * BASE...................Brings in Compass, Normalize, Susy, Variables and Mixins
     * HTML5 Bolierplate......HTML5 Boilerplate Styles
     * Elemental Styles.......Styles for HTML Elements
     * Utilities..............Reusabel Utility Classes
     * Content................Page Content
     * * Header...............Header Bar Styles
     * * Headline.............Headline / Welcome Area
     * * Main Content.........Main Content Area General Styles
     * * Sections.............Page Section Specific Styles
     * * * About
     * * * Work
     * * * Services
     * * * Crew
     * * * Clients
     * * * Contact
     * * * Portfolio
     * * Footer...............Footer Section of the Site aka Connect Panel
     * Helper Classes.........Things like clearfix, image replace
     */
   
#### Comments
###### Main Section Comments
    /*------------------------------------*\
        $TABLE OF CONTENTS
    \*------------------------------------*/
   Main Section Comments are wrapped like this. All caps proceeded with $ to allow for easier searching. Now when you command-f to find a section, you can search for $table and come up with the section instead of a class name or id.
   
    // Chrome Frame
    .chromeframe {
      margin: 0.2em 0;
      background: #ccc;
      color: #000;
      padding: 0.2em 0;
    }





    /*------------------------------------*\
        $ELEMENTAL STYLES
    \*------------------------------------*/

    body, p, li, table {
    	color:$text;
    }
 Main section comments should have 5 breaks preceeding them and 1 following.   
 
    
   
######    Section Comments




##### Borrowed Content
[Harry Robert's CSS Style](http://csswizardry.com/2012/04/my-html-css-coding-style/)

* Table of Contents
* Section Titles 