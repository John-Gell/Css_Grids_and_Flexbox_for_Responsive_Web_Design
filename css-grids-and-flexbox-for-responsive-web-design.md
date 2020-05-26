---
title: "Css Grids and Flexbox for Responsive Web Design"
tags: ""
---
# Responsive design

-   Defined by three characteristics:
    -   Flexible Grid-based layout
    -   Media queries (CSS3)
    -   Images that resize
        -   This is important for mobile and reducing data consumption based on the requirements of the system. 
-   Javascript is not required for Responsive design. it can be added later. 

# Floats

-   These are a 'hack', well supported but a hack
-   if you float you must clear 
    -   this is important to reduce errors down the road. 
-   Source ordering determined the display (no rearranging with css if using float) 
-   Major disadvantage
    -   standard row height. 

## Atribute Selector

-   This is close to a wildcard but has various selectors, look these up
-   rather than selecting an html tag or class, search the tags or classes for a specific attribute. 

```CSS
[class*="col-"] {
    position: relative;
}
```

\-What this snipit will do is select any node that constains the string "col-" 

### a trick for Attribute Selectors

```CSS
[href="http:"]
[href=".pdf"]
```

-   this will allow you to have a background image saying this link will go off site or to add a little PDF icon after each link leading to a pdf. 
    -   this is transcribed from a verbal description, syntax may be off. 

## Content Box Model

-   this is what the actual name is for the "Content, padding, border, margin" layout that comes up all the time. 
    -   the width is calculated using just the content. 
-   this is in oposition to the border box model. 

## Border Box Model

-   when you set width following setting the box-sizing parameter to `border-box` the `width:` property will size the node based on the sum of the margin, border, padding, and content, not just the content. 

[Link describing the border box model](https://www.paulirish.com/2012/box-sizing-border-box-ftw/)

```CSS
html {
    box-sizing: border-box;
}
/*initilizes the border-box property for the next step*/
*, /*the * is a wildcard or 'all' selector*/
*:before,
*:after{
    box-sizing: inherit;
}
/*causes all elements after this point to inherit the box-sizing property*/
```

-   this will apply the border-box to all elements on the page. 
