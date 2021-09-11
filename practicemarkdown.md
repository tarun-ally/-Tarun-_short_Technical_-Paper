# Report on CSS Flexbox and Grid
---
### CSS Flexbox

*CSS Flexbox is a layout mode in CSS3, which is used for designing and aligning between items in a container to control their arrangement. It arranges items in one-dimension. Either in row or in column. It is used for small scale layout like for header and footer.*

**Before applying CSS Flexbox** 


![Screenshot from 2021-08-22 00-39-38](https://user-images.githubusercontent.com/71551910/130367474-62de2ec2-42fb-4afc-814d-40ed66a24845.png)


```css


<style>
.nav-css{
    display: flex;
    background: skyblue;
    /* height: 50px; */
    align-items: center;
    gap: 20px;
}
.nav{
    background: skyblue;
    /* height: 50px; */
    align-items: center;
}

</style>
<div class="nav">
    <div>HOME</div>
    <div>ABOUT</div>
    <div>CONTACT</div>
    <div>SIGN UP</div>
    <div>SIGN IN</div>
</div>
```


**After applying CSS FLexbox**

<!-- <div class="nav-css"> -->
<!--     <div>HOME</div>
    <div>ABOUT</div>
    <div>CONTACT</div>
    <div>SIGN UP</div>
    <div>SIGN IN</div>
</div> -->

![Screenshot from 2021-08-22 00-39-42](https://user-images.githubusercontent.com/71551910/130367591-6a499f62-4a23-4b4d-94a5-73995d0f7797.png)

*By default, just by adding (display: Flex) its layout is changed to column.*
### Flexbox Properties
---
#### Flex Container

*Flex container is a block depending on the given value. It enables a flex context for all its direct children. It is a property for parent.*
``` css
.container {
  display: flex; 
}
```
#### Flex items
*Flex items are a property for children. Flex items are laid out in the source order. However, the order property controls the order in which they appear in the flex container.*
```css
.item {
  order: 50; 
}
```
#### Flex-direction
*Flex-direction establishes the main-axis, thus defining the direction flex items are placed in the flex container. Flex items as primarily laying out either in horizontal rows or vertical columns.*
``` css
.container {
  flex-direction: row;
}
```
### Flex-grow
*Flex-grow is the ability for a flex item to grow if necessary. It accepts a unitless value that serves as a proportion. It dictates what amount of the available space inside the flex container the item should take up.*
```css
.item {
  flex-grow: 4; /* default 0 */
}
```
#### Flex-Wrap
  *Flex items will all try to fit onto one line. we can change that and allow the items to wrap as needed with this property.*
  ```css
  .container {
  flex-wrap: wrap;
}
```
*wrap: flex items will wrap onto multiple lines, from top to bottom.*
#### Flex-Shrink
*Flex Shrink is the ability for a flex item to shrink if necessary.*
```css
.item{
    flex-shrink:20;
}
```
#### Flex-flow
*Flex flow is a shorthand for the flex-direction and flex-wrap properties, which together define the flex container’s main and cross axes. The default value is row nowrap.*
```css
.container {
    flex-flow: column wrap;
}

```
#### Flex
*Flex is the shorthand for flex-grow, flex-shrink and flex-basis combined. The default is 0 1 auto, but if you set it with a single number value, it’s like 1 0.*
```css
.item {
  flex: 1
}
```
*Flex will automatically set the flex-grow, flex-shrink and flex-basis.*
#### Align-self

*Align-self allows the default alignment to be overridden for individual flex Items.*
```css
.item {
  align-self: center;
}
```
*It will align flex Items to center.*
#### Align-Content
*align-content aligns a flex container’s lines within when there is extra space in the cross-axis,*
```css
.container {
  align-content: stretch;
}
```
*It will stretch lines to take up the remaining space.*

---

### CSS Grid

*CSS Grid is a collection of styles that allow us to control website pages layout based on rows and columns. It arranges items in two-dimension. It is mainly used for complex design, where user needed to design each item with different style. Example of these is [github](https://github.com/).*

```css
<style>
    .container {
    display: grid;
    grid-template-columns: 50px 50px 50px; */
    grid-gap: 10rem;
    grid-template-rows: 50px 50px;
}
.item {
    background-color: orange;
    border: 6px solid grey;
}
</style>
<div class="container">
    <div class="item item1"></div>
    <div class="item item2"></div>
    <div class="item item3"></div>
    <div class="item item4"></div>
    <div class="item item5"></div>
    <div class="item item6"></div>
</div>
```

**After applying CSS Grid**

![Screenshot from 2021-08-22 00-40-22](https://user-images.githubusercontent.com/71551910/130367625-ce30aae2-ba64-40eb-b0b5-2fc3403af8d8.png)


<div class="container">
    <div class="item item1"></div>
    <div class="item item2"></div>
    <div class="item item3"></div>
    <div class="item item4"></div>
    <div class="item item5"></div>
    <div class="item item6"></div>
</div>

*By applying CSS grid we can make changes to multi-column as well as multi-row at same time.*

### Grid Properties
#### Display
*Display defines the element as a grid container and establishes a new grid formatting context for its contents.*
```css
.container {
  display: grid;
}
```
*grid – generates a block-level grid.*
#### Grid-column
*Grid-column shorthand for grid-column-start + grid-column-end.*
```css
.item {
  grid-column: 3/ span 2;
}
```
#### Grid-row
*Grid-row is a shorthand for grid-row-start + grid-row-end.*
```css

.item {
  grid-row: third-line / 4 ;
}
```
#### Grid-area
*Grid-area gives an item a name, so that it can be referenced by a template created with the grid-template-areas property. Also, this property can be used as an even shorter shorthand for grid-row-start + grid-column-start + grid-row-end + grid-column-end.*
```css
.item-d {
  grid-area: header;
}
```
#### Justify-self
*Justify-self aligns a grid item inside a cell along the inline (row) axis. This value applies to a grid item inside a single cell.*
```css
.item {
  justify-self: start ;
}
```
*It will aligns the grid item to be flush with the start edge of the cell.*

#### Align-self
*Align-self aligns a grid item inside a cell along the block (column) axis (as opposed to justify-self which aligns along the inline (row) axis). This value applies to the content inside a single grid item.*
```css
.item-a {
  align-self: end;
}
```
*It will aligns the grid item to be flush with the start edge of the cell.*
#### Justify-content
*Justify-content property aligns the grid along the inline (row) axis.*
```css
.container {
  justify-content: end;    
}
```
*It will aligns the grid to be flush with the end edge of the grid container.*


**Reference**

*Website link:*
[Section](https://www.section.io/engineering-education/css-flexbox-vs-css-grid/),
[CSS-TRICKS](https://css-tricks.com/snippets/css/a-guide-to-flexbox/#flexbox-properties)

