# CSS Grid
CSS Grid is a new module that brings two-dimensional grid system to CSS for the first time.

## Common terms in CSS Grid
* **Grid line** => this is the line seperate the grid rows and also the grid columns. It started from one and all the way to the number of rows plus one or the number of columns plus one

* **Gutter** => This is the actual space between the rows or the columns. The row gutters can be different from the column gutters.

* **Grid Track** => This is the space between two grid lines or two grid columns. 

* **Grid area** => This is the area between two vertical and two horizontal gird lines.

* **Grid cell** => This is the area between two adjacent grid lines and two adjacent column lines.


## CSS GRID PROPERTIES

### For Containers
1. grid-templates
    * grid-template-rows
    * grid-template-columns
    * grid-template-areas

2. grid-gap
    * grid-row-gap
    * grid-column-gap

3. 
    * justify-items
    * align-items
    * justify-content
    * align-content

4. 
    * grid-auto-rows
    * grid-auto-columns
    * grid-auto-flow


### Item
1. grid-row
    * grid-row-start
    * grid-row-end

2. grid-column
    * grid-column-start
    * grid-column-end

*The above grid-row and grid-column can also be define using **grid-area***

3. 
    * justify-self
    * align-self

4. order


<!-- MORE INFO ON CSS GRID -->

### GRID-TEMPLATE-AREAS
We specify a string that represent our layout with names that we'll give our
grid items
e.g
"head head head head"
"content content content content"
"story story story story"
"foot foot foot foot"

We can then name our grid items to match the above using grid-area property.
When naming our grid-template-areas, we must fill up our entire grid container
with content we want to display if not it will not work correctly.
To leave an empty space we'll have to use a dot in the position we want to leave
empty


### EXPLICIT AND IMPLICIT GRID
The part of the grid rows and columns we defined are called explicit grids. If the
grid rows and columns we defined cannot fit the grid items we have, then css grid
implicitly create other rows and columns to fit the remaining grid items. The grid
area that grid layout automatically create when it need to fit the remaining grid
items is known as implicit grid.

#### Styling implicit grids
We can style implicit grid using grid-auto-columns and grid-auto-rows.


### CHANGING THE IMPLICIT FLOW OF OUR GRID ITEMS
By default the flow of our implicit grids are set to row, to change it to column
we'll use the grid-auto-flow property and sets it to column. When we set it to
column the implicit grid items will now be added to the columns and not rows.


### ALIGNING GRID ITEMS IN GRID AREAS
We align grid items in grid areas using aligin-items and justify-items on the grid
container to apply to all grid items. To target a specific grid item we use align-self
and justify-self properties.


### ALIGNING ITEMS PROPERTIES

* **align-items**: Align grid items vertically, used on the grid-container to target
all grid items

* **justify-items**: Align grid items horizontally, used on the grid-container to target
all grid items

Align-items and justify-content possible values: stretch, start, end, center, stretch being
the default

<!-- Targetting individual grid items -->
* **justify-self**: Align a grid item horizontally, use to target a single grid item
* **justify-self**: Align a grid item horizontally, use to target a single grid item

Align-self and justify-self possible values: stretch, start, end, center, stretch being
the default



### ALIGN TRACKS IN THE GRID CONTAINER
If we specify a height and width to the grid container and the tracks which are both
the rows and columns cannot occupy the entire container, we can align the tracks with
the spaces that remain in the grid container.

#### PROPERTIES TO ALIGN THE GRID TRACKS
* **align-content**: Align the tracks along the vertical axis
* **justify-content**: Align the tracks along the horizontal axis

Possible values of align-content and justify content: center, start, end, space-between,
space-around, space-evenly.


### HINTS
When we use -content as the ending of the property for aligning, we are aligning the tracks but
when we use -items, we are actually aligining the items in the grid area.
Also when we use aligin- we are aligning on the vertical axis and we use justify we mean the
horizontal-axis.
