# Report on CSS Flexbox and Grid
---
### CSS Flexbox

*CSS Flexbox is a layout mode in CSS3, which is used for designing and aligning between items in a container to control their arrangement. It arranges items in one-dimension. Either in row or in column. It is used for small scale layout like for header and footer.*

**Before applying CSS Flexbox** 
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

<div class="nav-css">
    <div>HOME</div>
    <div>ABOUT</div>
    <div>CONTACT</div>
    <div>SIGN UP</div>
    <div>SIGN IN</div>
</div>

*By default, just by adding (display: Flex) its layout is changed to column.*

### CSS Grid
---
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

*By applying CSS grid we can make changes to multi-column as well as multi-row at same time.*

**Reference**

*Website link:*
[Section](https://www.section.io/engineering-education/css-flexbox-vs-css-grid/)

