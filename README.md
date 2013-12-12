styleguide
==========

<h2>SASS Style Guide</h2>


<h3>Naming Patterns</h3>
SASS variables need a constent naming scheme. Variables need to be semantic enough to be understood, so that it adds an extra dimension of clarity to the thing its defining but provide enough abiguity so that the variable value could be changed without having to change the name of the variable. 

$primary-blue: primary is irrelevant to understanding what the variable represents.

$blue-primary: is better, but primary is again redundant. If we assume that something with a single name like $blue is primary.

$blue-alt: this is a better because it implies that this is an alternative blue to the primary, probably a variation but gives no indication of what the alternative is.

$blue-light: this is good because it instantly conveys that this is a lighter shade of the primary blue color being used.

$blue-light-10: this would be used if the blue was a 10% lightening of the primary blue it only refers to a single shade of blue, not a variable that can contain any blue lighter than the original $blue. Instead of $blue-light-10 the designer should just use lighten($blue, 10%) as its almost the same number of characters.

If there's is a completely separate blue being used a using any number of descriptive color names, azure, lightblue, teal, oceanblue etc. are better than using primary-blue, secondary-blue etc because those names do not help explain what is being represented. 

<h3>Repeatable Styles</h3>
A placeholder class should be used on anything that is a repeatable style. Chances are that the designer wants the same border-radius on anything that has a border radius. Creating a class .border-radius and applying it to anything that has a border-radius is tedious. Creating the placeholder class %border-radius and @extend-ing it is the better option because it allows the border radius of all objects to be set by a single line of code, but doesn't require horibbly redundanct classes.

%border_radius

%emboss

%text_emboss

These are all placeholder classes that instantly convey what they are and can be reused many times classes across a site.

<h3>Dimensions</h3>
Fixed dimensions should be used as often as possible. Using a variable like $padding to serve as the default padding between objects creates visual rhythm and consistentcy but also makes it easy to set things in a vertical grid. If a div needs to be flush against the edge of a containing box that has padding. If the variable $padding was used then the designer can simply apply a negative marging of -$padding to of set it the correct distance. Additionaly for maintaing vertical alignment things like $padding/2 can be used to apply space above and below an object. 

<h3>Dashes for prefixes only</h3>
A dash should be used to show parent child relationships. A good example would be .left_sidebar and .left_sidebar-inner. By prefixing -inner, with left_sidebar instantly tells what the container's parent element is and allows there to be multiple "inner" classes that are unique. Using brackets [class^="left_sidebar-"] can allow naming patterns to be applied to anything that has the prefix. Never more than two prefixes: two dashes.



<h3>Grid Naming Convention</h3>
container > grid > col- > module


<h3>OBEY THE INCEPTION RULE</h3>
<em>Mostly because its clever</em>
