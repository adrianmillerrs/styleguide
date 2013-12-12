styleguide
==========

<h2>SASS Style Guide</h2>

Naming Convention:
Underscore for multi word names left_side_bar

Dash for greater specificity left_side_bar-container

Variable Naming:
Naming always moves from more general to more specific.

lightblue $light_blue

blue -$blue

$blue-light: lighten($blue, 10%);

lightblue - $blue-light

gray - $gray
darkgray - $gray-light

Plural(s) classes always contain singular classes

buttons > button

links > link

position and spacing classes should be separate from aesthetics.

<button class="large blue"></button>

large = specific size of the element
blue = applies coloring to element
