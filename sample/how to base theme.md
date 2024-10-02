---
marp: true
theme: basetheme
paginate: true
footer: Replace this with your desired footer text 
header: '![lupo](media/logo-dark.png)'
---
<!-- _class: slide-cover
_header: '![lupo](media/logo-light.png)' -->

![](media/lupo-light.png)

# The Great Base Theme

## Step by step

<!-- 
Follow this guide to easily start with Lupo's basic template.
-->

---
<!-- _class: slide-cover -->

# Your .MD File Basics 

## The First Steps 

<!-- 
Lets start with what you can do in your markdown file. 
-->

---


```
---
marp: true
theme: basetheme
paginate: true
footer: Replace this with your desired footer text 
header: '![lupo](media/logo-dark.png)'
---
```




<!-- 
These is the front-matter syntax, it must always be the first thing of Markdown, and between the dash rulers.
marp: true is what gives whatevcer you write below, the slide format, dont remove it.
theme: basetheme is what applies the basetheme.css, if you have a theme prepared you could change it following a couple extra steps you can find in the documentation.
paginate accepts values of true or false, false will not show page numbers on any of the slides
footer accepts text, you can replace the text up there and it will be changed in all slides
header accepts images, you can replace it with your logo
-->

---



```
<!-- backgroundColor: aqua -->

This page has aqua background.

---

The second page also has same color.
```



<!-- 
Then you could use "local directives", this will make changes to the slide you are applying it to and to all the following slides. These are written as comments at the beggining of the slide.
-->

---



```
<!-- _backgroundColor: aqua -->

Add underscore prefix `_` to the name of local directives.

---

The second page would not apply setting of directives.
```



<!-- 
You can use "spot directives" if you want to apply it only to the slide you are corrently on, it's the same to "local directives" but with a underscore at the beginning. 
-->

---



paginate	Show page number on the slide if you set true.
header	Specify the content of slide header.
footer	Specify the content of slide footer.
class	Specify HTML class of slide’s `<section>` element.
backgroundColor	Setting background-color style of slide.
backgroundImage	Setting background-image style of slide.
backgroundPosition	Setting background-position style of slide.
backgroundRepeat	Setting background-repeat style of slide.
backgroundSize	Setting background-size style of slide.
color	Setting color style of slide.



<!-- 
These are the local directives available. You can turn on and off the pagination of each slide independently. In this template you have the logo for the header, depending on the color of the background it might not be visible, in this cases you could have another version of your logo in a color that has better contrast and use it in these slides. The class local directive is similar to the sort of template you want to apply to the slide, it defines how different elements like the headers, text and background colors will show up, I'll detail this in the next slides.
-->

---
<!-- _class: slide-cover -->

# The Templates

## AKA Class Local Directive 

<!-- 
Now, let me explain how you can call the templates
-->

---


```
<!-- _class: slide-test-colors -->
<!-- _class: slide-cover -->
<!-- _class: slide-onethirdleft-twothirdsright -->
<!-- _class: slide-header-onethirdleft-twothirdsright -->
<!-- _class: slide-header-halfleft-halfright -->
<!-- _class: slide-definition -->
<!-- _class: slide-header-content -->
<!-- _class: slide-header-subheader-content -->
<!-- _class: slide-image-rightnote -->
<!-- _class: slide-image-centerednote -->
<!-- _class: slide-thanks -->
<!-- _class: slide-video -->
<!-- _class: slide-demo -->
```




<!-- 
These are the class local directives that are already defined for you, think of these as the templates of the slides. 
-->

---

<!-- _class: slide-cover
_footer: "" 
_header: "" 
_paginate: false 
_backgroundImage: url(media/backgroud.jpg) -->

```
<!-- _class: slide-cover 
_footer: "" 
_header: "" 
_paginate: false 
_backgroundImage: '![lupo](media/logo-dark.png)'-->
```

<!-- 
You can add more than one local directive to a slide, just write each one in an independent line, like this. If you want to leave the footer or header empty just write two double qoutes. You can also add a background image for an even more personalized look.
-->

---

<!-- _class: slide-cover -->

# Let's make it look personalized

## By adding your fonts and colors

<!-- 
This base template has been designed so that with just a couple of changes to the .CSS, your presentation will look more personalized.
-->

---


<!-- _class: slide-header-onethirdleft-twothirdsright -->

# Leave theses lines alone!

<contentarea style="font-size: pt;">

```
@import 'default';

/* required for video, do not delete */
video {
    position: fixed;
    right: 0;
    bottom: 0;
    min-width: 100%;
    min-height: 100%;
}

img {
    background-color: transparent !important;
    object-fit: cover;
    display: flex;
    align-items: center;
    justify-content: center;
}
```

</contentarea>

<!-- 
Start by opening the file basetheme.css. inside the folder "themes".
When you open it, at the beginnig you will see an @import and a comment that says "required for video, do not delete". These lines of code are used for importing the theme and for the video generation, do not modify them or delete them.
-->

---
<!-- _class: slide-header-halfleft-halfright -->

# We make it easier for you

<left>

``` css
/* Replace with your font */
@import url('https://fonts.googleapis.com/
css2?family=Nunito:wght@300;400;500;700&fa
mily=Roboto+Mono:wght@300;400;500;700&famil
y=Roboto+Slab:wght@300;400;500;700&family=R
oboto:wght@300;400;500;700&display=swap');

/* Replace with your font and colors */
:root {
    --primary-font: 'Poppins', sans-serif;
    --secondary-font: 'Nunito', sans-serif;
    --code-font: 'Roboto Mono', monospace;

    --lightmode-background: #FFFFFF;
    --lightmode-text: #333333;
    --lightmode-accent: #CCCCCC;
    --darkmode--background: #333333;
    --darkmode--text: #CCCCCC;
    --darkmode--accent: #666666;
}
```

</left>

<right>

1. Add your font:
    1. Replace the `@import url` link
    1. Or use the `@font-face` rule
1. Replace:
    1. Font names 
        1. Poppins, Nunito, and Roboto Mono
    2. HEX code of colors 
        1. #FFFFFF, #333333, #CCCCCC, #333333, #CCCCCC, and #666666
1. Save the CSS file.
1. Fonts and colors should be updated

</right>

<!-- 
To use the colors and fonts of your choice go to the "base theme css". There, around line 23, you will see a section where you can add your font and colors that looks like the image on the left. 

If you're using a font hosted by services like Google Fonts, just replace the link inside the "@ import url". However, if you're using a font that you're hosting yourself, you can use the "@ font face" rule.

Now, start changing the names of the fonts (in this example Poppins, Nunito, and Roboto Mono) and the HEX code of the colors.

"Primary font" refers to the font used in headers. "Secondary font" is the font used in sub headers and in regular text.  "Code font" is the font that is going to display in case you show code or code blocks.

About the colors, there are main and dark. Main are the ones shown as a light theme, dark refers to the colors uses as if it was a dark theme. So "main background", "main text", and "main accent" would be the colors displayed in your light theme background, light theme text and light theme accent. While "dark background", "dark text", and "dark accent" would be the colors displayed in your dark theme background, light theme text and light theme accent.

Important, don't change the name after the two dashes, only change the name of the font. These names are used all around the CSS to call the fonts and colors you want to use, if you change this names, youir style wont display correctly.
-->


---

<!-- _class: slide-test-colors 
_footer: "" 
_header: "" 
_paginate: false -->

<left>

![w:150px](media/logo-dark.png)
# main text
## main accent

</left>

<right>

![w:150px](media/logo-light.png)
# dark text color
## dark accent color

</right>

<!-- 
This slide called "test colors" will help you test how text and logos wil look over background colors. To be able to see the logos replace the files in sample/media called logo-dark.png and logo-light.png with your logos in dark color and light color.s
-->







---
<!-- _class: slide-cover -->

# Base theme templates

## Two ways to use them

<!-- 
You can use preset templates in two different way, copy-pasting or snippets
-->

---
<!-- _class: slide-header-halfleft-halfright -->

# 1. Copy and Paste

<left>

As the title says, open the 'base-theme-sample.md' file and copy and paste the template you want to use

</left>

<divline> </divline>

<right>

* Pros: 
    * Can visually see what you will get
    * Have an example of contents

* Cons:
    * If the file is modified you will get errors 

</right>

<!-- 

-->

---
<!-- _class: slide-header-onethirdleft-twothirdsright -->

# 2. Snnipets

<left>

The other option is using snnipets. 

If you are working with VSCode you can use snippets. To use snnipets:
1. Type `slide-`  
2. Press Enter or Tab
3. And start replacing the prompted text with what you want to show


</left>


<right>

* Pros: 
    * 

* Cons:
    *  

</right>

<!-- 

-->


---
<!-- _class: slide-cover -->

# What if things don't fit

## You can make extra adjustments

---
<!-- _class: slide-onethirdleft-twothirdsright -->

<left>

# Accepts html = Endless Possibilities

</left>

<right>

* Already in your templates like `<left>`, `<right>`, or `<box>`
* Need to modify a text?
    * `This text is very important and I need to make it more striking`
    * This text is very important and I need to make it more striking
    * `<p style="font-size: 40px; color: red; font-weight: bold; text-transform: uppercase;"> This text is very important and I need to make it more striking </p>`
    * <p style="font-size: 40px; color: red; font-weight: bold; text-transform: uppercase;"> This text is very important and I need to make it more striking </p>

</right>

<!-- Markdown and CSS alone have their limitations, luckily, theres html. You can make a mix of markdown and html to help you design better slides.
You can see one case in some of the already prepared slide templates, where you can see elements like <left> or <right>. 
Also in some case you might have a header that is too long and won't fit, you can use html to modify the font size -->


---

# Thanks!

## Do you have any questions?

### help@lupo.ai 