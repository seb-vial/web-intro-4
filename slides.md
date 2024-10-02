---
theme: light-icons
image: ./images/intro.jpg
title: Web development - Introduction | Part 4
transition: slide-left
mdc: true
layout: intro
download: true
favicon: "https://scratchmy.dev/favicon.ico"
---

<div class="mb-4 absolute top-20 left-12">
  <span class="text-6xl text-teal-400 font-500" >
    Web development<light-icon icon="code"/>
  </span>
  <div class="text-4xl text-white text-opacity-60 font-300 uppercase" >
    Introduction – Part 4
  </div>
</div>

<div class="mb-4 absolute bottom-4 right-12">
  <div class="flex gap-x-4 items-center">
    <div class="rounded-full p-0.5 shadow-lg shadow-zinc-800/5 ring-1 backdrop-blur bg-white ring-white/10">
      <img src="/images/profile.webp" sizes="4rem" class="rounded-full object-cover h-16 w-16" alt="Profile picture" width="400" height="400" loading="lazy" decoding="async">
    </div>
    <div class="flex flex-col">
      <p class="!my-1 text-xl">Sébastien VIALLEMONTEIL</p>
      <p class="!my-1">Full stack web developer</p>
      <a href="mailto:sebastien.viallemonteil@institut-agro.fr"><light-icon icon="mail" class="inline-block mb-0.5"/> sebastien.viallemonteil@institut-agro.fr</a>
    </div>
  </div>
</div>

---
layout: dynamic-image
image: ./images/flexbox.jpg
equal: false
left: false
---

# Flexbox
Time to stretch and work on your mobility

Flexbox is a new type of **display**. Compared to other kinds of display, flexbox will affect how child elements behave. It rests on **four principles**.

<v-clicks>

- **Positioning**: There are **two axis** to position child elements (**flex-items**), **main** axis and **cross** axis. By default the main axis is **horizontal** and cross axis is **vertical**. This behavior can be changed.
- **Alignment**: Align child elements on both **main** and **cross** axis.
- **Order**: Change the default order in which child elements will be displayed, whatever their initial position is in the HTML code.
- **Flexible sizing**: Manage how free space should be taken by child elements

</v-clicks>

<ComplementaryMessage type="alert" bordered>The <strong>display</strong> value of child elements is ignored</ComplementaryMessage>

---
layout: dynamic-image
image: ./images/flexbox.jpg
equal: false
left: false
---

# Flexbox
Managing direction (axis)

<Transform scale="0.95">

```css {*}{lines:true}
.my-flexible-element {
  display: flex;
  /* Positioning child elements horizontaly by default */
  flex-direction: row; /* <== Default value */
}
```

<div v-click="2">

```css {*}{lines:true}
.my-flexible-element {
  display: flex;
  /* Positioning child elements verticaly */
  flex-direction: column;
}
```

</div>
<div v-click="3">

```css {*}{lines:true}
.my-flexible-element {
  display: flex;
  /* Positioning child elements horizontaly in reverse order */
  flex-direction: row-reverse;
}
```

</div>
<div v-click="4">

```css {*}{lines:true}
.my-flexible-element {
  display: flex;
  /* Positioning child elements verticaly in reverse order */
  flex-direction: column-reverse;
}
```

</div>
</Transform>
<div v-motion v-click="[1,2]" :initial="{x: 999, y: -999}" :enter="{x: 570, y: -330}" class="absolute max-w-1/3 p-2 bg-gray-700 text-white dark:text-gray-800 dark:bg-white rounded-md border-2 border-teal-600">
  <div class="p-2 flex border border-red space-x-1">
    <div class="p-2 border border-dotted border-blue">Hey I’m block</div>
    <div class="p-2 border border-dotted border-green">And me inline</div>
    <div class="p-2 border border-dotted border-purple">Inline-block is my name</div>
  </div>
</div>

<div v-motion v-click="[2,3]" :initial="{x: 999, y: -999}" :enter="{x: 570, y: -330}" class="absolute max-w-1/3 p-2 bg-gray-700 text-white dark:text-gray-800 dark:bg-white rounded-md border-2 border-teal-600">
  <div class="p-2 flex flex-col border border-red space-y-1">
    <div class="p-2 border border-dotted border-blue">Hey I’m block</div>
    <div class="p-2 border border-dotted border-green">And me inline</div>
    <div class="p-2 border border-dotted border-purple">Inline-block is my name</div>
  </div>
</div>

<div v-motion v-click="[3,4]" :initial="{x: 999, y: -999}" :enter="{x: 570, y: -330}" class="absolute max-w-1/3 p-2 bg-gray-700 text-white dark:text-gray-800 dark:bg-white rounded-md border-2 border-teal-600">
  <div class="p-2 flex flex-row-reverse border border-red">
    <div class="p-2 border border-dotted border-blue ml-1">Hey I’m block</div>
    <div class="p-2 border border-dotted border-green ml-1">And me inline</div>
    <div class="p-2 border border-dotted border-purple">Inline-block is my name</div>
  </div>
</div>

<div v-motion v-click="4" :initial="{x: 999, y: -999}" :enter="{x: 570, y: -330}" class="absolute max-w-1/3 p-2 bg-gray-700 text-white dark:text-gray-800 dark:bg-white rounded-md border-2 border-teal-600">
  <div class="p-2 flex flex-col-reverse border border-red">
    <div class="p-2 border border-dotted border-blue mt-1">Hey I’m block</div>
    <div class="p-2 border border-dotted border-green mt-1">And me inline</div>
    <div class="p-2 border border-dotted border-purple">Inline-block is my name</div>
  </div>
</div>

---
layout: dynamic-image
image: ./images/flexbox.jpg
equal: false
left: false
---

# Flexbox
That’s a wrap

```css {*}{lines:true}
.my-flexible-element {
  display: flex;
  flex-wrap: nowrap; /* <== Default value */
}
```

<div v-click="2">

```css {*}{lines:true}
.my-flexible-element {
  display: flex;
  /* We allow wraping */
  flex-wrap: wrap;
}
```

</div>

<div v-click="3">

```css {*}{lines:true}
.my-flexible-element {
  display: flex;
  /* We allow wraping in reverse */
  flex-wrap: wrap-reverse;
}
```

</div>

<div v-motion v-click="[1,2]" :initial="{x: 999, y: -999}" :enter="{x: 570, y: -310}" class="absolute w-1/3 p-2 bg-gray-700 text-white dark:text-gray-800 dark:bg-white rounded-md border-2 border-teal-600">
  <div class="p-2 flex border border-red space-x-1 max-w-40">
    <div class="p-2 border border-dotted border-blue">I am a very long text which will cause my siblings overflow our flex container</div>
    <div class="p-2 border border-dotted border-green">I’m out of bounds</div>
    <div class="p-2 border border-dotted border-purple">Me too !</div>
  </div>
</div>

<div v-motion v-click="[2,3]" :initial="{x: 999, y: -999}" :enter="{x: 570, y: -310}" class="absolute w-1/3 p-2 bg-gray-700 text-white dark:text-gray-800 dark:bg-white rounded-md border-2 border-teal-600">
  <div class="p-2 flex flex-wrap border border-red max-w-40">
    <div class="p-2 border border-dotted border-blue">I am a very long text which should cause my siblings overflow our flex container</div>
    <div class="p-2 border border-dotted border-green">But it doesn’t</div>
    <div class="p-2 border border-dotted border-purple">That’s right</div>
  </div>
</div>
<div v-motion v-click="[3]" :initial="{x: 999, y: -999}" :enter="{x: 570, y: -310}" class="absolute w-1/3 p-2 bg-gray-700 text-white dark:text-gray-800 dark:bg-white rounded-md border-2 border-teal-600">
  <div class="p-2 flex flex-wrap-reverse border border-red max-w-40">
    <div class="p-2 border border-dotted border-blue">I am a very long text which should cause my siblings overflow our flex container</div>
    <div class="p-2 border border-dotted border-green">But it doesn’t</div>
    <div class="p-2 border border-dotted border-purple">That’s right</div>
  </div>
</div>

<div v-click="4">
  <ComplementaryMessage bordered>NB: <strong>flex-flow</strong> combines <strong>flex-direction</strong> and <strong>flex-wrap</strong> rules.<br>Example: <strong>"flex-flow: column wrap-reverse;"</strong></ComplementaryMessage>
</div>

---
layout: dynamic-image
image: ./images/flexbox.jpg
equal: false
left: false
---

# Flexbox
Aligning on the main axis

The main axis depends on which direction is set for the flex container (row or column).

<Transform scale="0.95">
<div v-click="1">

```css {*}{lines:true}
.my-flexible-element {
  display: flex;
  /* Setting alignment on main axis, horizontal in this case */
  justify-content: flex-start; /* <== Default value */
}
```

</div>

<div v-click="2">

```css {*}{lines:true}
.my-flexible-element {
  display: flex;
  /* Equal space between child elements on the main axis */
  justify-content: space-between;
}
```

</div>

<div v-click="3">

```css {*}{lines:true}
.my-flexible-element {
  display: flex;
  flex-direction: column; /* Main axis is vertical now */
  justify-content: center; /* Centered on the main axis */
}
```

</div>
</Transform>

<div v-motion v-click="[1,2]" :initial="{x: 999, y: -999}" :enter="{x: 570, y: -250}" class="absolute w-1/3 p-2 bg-gray-700 text-white dark:text-gray-800 dark:bg-white rounded-md border-2 border-teal-600">
  <div class="p-0.5 flex border border-red space-x-0.5 text-xs">
    <div class="p-2 border border-dotted border-blue">First child</div>
    <div class="p-2 border border-dotted border-green">Second child</div>
    <div class="p-2 border border-dotted border-purple">Third child</div>
  </div>
</div>

<div v-motion v-click="[2,3]" :initial="{x: 999, y: -999}" :enter="{x: 570, y: -250}" class="absolute w-1/3 p-2 bg-gray-700 text-white dark:text-gray-800 dark:bg-white rounded-md border-2 border-teal-600">
  <div class="p-0.5 flex justify-between border border-red space-x-0.5 text-xs">
    <div class="p-2 border border-dotted border-blue">First child</div>
    <div class="p-2 border border-dotted border-green">Second child</div>
    <div class="p-2 border border-dotted border-purple">Third child</div>
  </div>
</div>

<div v-motion v-click="[3]" :initial="{x: 999, y: -999}" :enter="{x: 570, y: -250}" class="absolute w-1/3 h-50 p-2 bg-gray-700 text-white dark:text-gray-800 dark:bg-white rounded-md border-2 border-teal-600">
  <div class="p-0.5 flex flex-col justify-center border border-red space-y-0.5 text-xs h-full">
    <div class="p-2 border border-dotted border-blue">First child</div>
    <div class="p-2 border border-dotted border-green">Second child</div>
    <div class="p-2 border border-dotted border-purple">Third child</div>
  </div>
</div>
<div v-click="4" class="-mt-2">More on <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/justify-content">justify-content</a></div>

---
layout: dynamic-image
image: ./images/flexbox.jpg
equal: false
left: false
---

# Flexbox
Aligning on the cross axis

The cross axis depends on which direction is set for the flex container (row or column).

<Transform scale="0.95">
<div v-click="1">

```css {*}{lines:true}
.my-flexible-element {
  display: flex;
  /* Setting alignment on cross axis, vertical in this case */
  align-items: stretch; /* <== Default value */
}
```

</div>

<div v-click="2">

```css {*}{lines:true}
.my-flexible-element {
  display: flex;
  /* Pushing child elements at the end of the cross axis */
  align-items: flex-end;
}
```

</div>

<div v-click="3">

```css {*}{lines:true}
.my-flexible-element {
  display: flex;
  flex-direction: column; /* Main axis is vertical now */
  align-items: center; /* Centered on the cross axis */
}
```

</div>
</Transform>

<div v-motion v-click="[1,2]" :initial="{x: 999, y: -999}" :enter="{x: 570, y: -250}" class="absolute w-1/3 p-2 bg-gray-700 text-white dark:text-gray-800 dark:bg-white rounded-md border-2 border-teal-600">
  <div class="p-0.5 flex border border-red space-x-0.5 text-xs min-h-20">
    <div class="p-2 border border-dotted border-blue">First child</div>
    <div class="p-2 border border-dotted border-green">Second child</div>
    <div class="p-2 border border-dotted border-purple">Third child</div>
  </div>
</div>

<div v-motion v-click="[2,3]" :initial="{x: 999, y: -999}" :enter="{x: 570, y: -250}" class="absolute w-1/3 p-2 bg-gray-700 text-white dark:text-gray-800 dark:bg-white rounded-md border-2 border-teal-600">
  <div class="p-0.5 flex items-end border border-red space-x-0.5 text-xs min-h-20">
    <div class="p-2 border border-dotted border-blue">First child</div>
    <div class="p-2 border border-dotted border-green">Second child</div>
    <div class="p-2 border border-dotted border-purple">Third child</div>
  </div>
</div>

<div v-motion v-click="[3]" :initial="{x: 999, y: -999}" :enter="{x: 570, y: -250}" class="absolute w-1/3 h-50 p-2 bg-gray-700 text-white dark:text-gray-800 dark:bg-white rounded-md border-2 border-teal-600">
  <div class="p-0.5 flex flex-col items-center border border-red space-y-0.5 text-xs h-full">
    <div class="p-2 border border-dotted border-blue">First child</div>
    <div class="p-2 border border-dotted border-green">Second child</div>
    <div class="p-2 border border-dotted border-purple">Third child</div>
  </div>
</div>
<div v-click="4" class="-mt-2">More on <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/align-items">align-items</a></div>

---
layout: dynamic-image
image: ./images/flexbox.jpg
equal: false
left: false
---

# Flexbox
Aligning one or more flex-items on the cross axis

With ***align-self***, child items can be aligned differently from their sibling on the cross axis.

<div v-click>

```css {*}{lines:true}
.my-flexible-element {
  display: flex;
  flex-direction: column;
  /* Setting alignment on cross axis, horizontal in this case */
  align-items: stretch; /* <== Default value */
}
.my-flexible-element .second-child {
  /* This flex item is going to align differently on the cross axis */
  align-self: center;
}
```

<div v-motion :initial="{x: 999, y: -999}" :enter="{x: 570, y: -205}" class="absolute w-1/3 h-50 p-2 bg-gray-700 text-white dark:text-gray-800 dark:bg-white rounded-md border-2 border-teal-600">
  <div class="p-0.5 flex flex-col border border-red space-y-0.5 text-xs h-full">
    <div class="p-2 border border-dotted border-blue">First child</div>
    <div class="p-2 border border-dotted border-green self-center">Second child</div>
    <div class="p-2 border border-dotted border-purple">Third child</div>
  </div>
</div>
</div>

<div v-click>More on <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/align-self">align-self</a></div>
<ComplementaryMessage type="alert" bordered><strong>align-self</strong> is set on flex items (child elements), not the flex container</ComplementaryMessage>

---
layout: dynamic-image
image: ./images/flexbox.jpg
equal: false
left: false
---

# Flexbox
Space between elements on the cross axis

If for some reason there are multiple rows or columns on the cross axis (depending on the main direction), space between flex items is managable.

<div v-click>

```css {*}{lines:true}
.my-flexible-element {
  display: flex;
  flex-flow: column wrap; /* wrap is needed */
  align-content: space-evenly;
}
```

<div v-motion :initial="{x: 999, y: -999}" :enter="{x: 570, y: -205}" class="absolute w-1/3 h-40 p-2 bg-gray-700 text-white dark:text-gray-800 dark:bg-white rounded-md border-2 border-teal-600">
  <div class="p-0.5 flex flex-col flex-wrap content-evenly border border-red text-xs h-full gap-0.5">
    <div class="p-2 border border-dotted border-blue">First child</div>
    <div class="p-2 border border-dotted border-green">Second child</div>
    <div class="p-2 border border-dotted border-purple">Third child</div>
    <div class="p-2 border border-dotted border-yellow">Fourth child</div>
    <div class="p-2 border border-dotted border-sky">Fifth child</div>
    <div class="p-2 border border-dotted border-teal">Sixth child</div>
  </div>
</div>
</div>
<div v-click>More on <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/align-content">align-content</a></div>

---
layout: dynamic-image
image: ./images/flexbox.jpg
equal: false
left: false
---

# Flexbox
Set your flex items in order

Using flexbox display, you are free to rearrange the flex items, change the position of one or more of them without changing their order in the HTML code.
By default flex items have an **order** of **0**.

<div v-click>

```css {*}{lines:true}
.my-flexible-element {
  display: flex;
}
.my-flexible-element .third-element {
  order: -1;
}
.my-flexible-element .first-element {
  order: 1;
}
```

<div v-motion :initial="{x: 999, y: -999}" :enter="{x: 570, y: -120}" class="absolute w-1/3 p-2 bg-gray-700 text-white dark:text-gray-800 dark:bg-white rounded-md border-2 border-teal-600">
  <div class="p-0.5 flex border border-red text-xs gap-0.5">
    <div class="p-2 border border-dotted border-blue order-1">First child</div>
    <div class="p-2 border border-dotted border-green">Second child</div>
    <div class="p-2 border border-dotted border-purple order-[-1]">Third child</div>
  </div>
</div>
</div>
<div v-click>More on <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/order">order</a></div>
<ComplementaryMessage bordered>Negative order will push the flex item to the start of the container, positive order will push it to the end.</ComplementaryMessage>

---
layout: dynamic-image
image: ./images/flexbox.jpg
equal: false
left: false
---

# Flexbox
Allowing flex items to shrink or grow

If there is free space in your flex container, you can allow flex items to take it.

<div v-click>

```css {*}{lines:true}
.my-flexible-element {
  display: flex;
}
.my-flexible-element .third-element {
  /* Allowing flex item to shrink if necessary, yes by default */
  flex-shrink: 1; /* 1 by default */
  /* Allowing flex item to grow,
    taking the remaining space in its container */
  flex-grow: 1; /* 0 by default */
  /* Setting the default size of the flex item */
  flex-basis: auto; /* auto by default */
}
```

<div v-motion :initial="{x: 999, y: -999}" :enter="{x: 570, y: -150}" class="absolute w-1/3 p-2 bg-gray-700 text-white dark:text-gray-800 dark:bg-white rounded-md border-2 border-teal-600">
  <div class="p-0.5 flex border border-red text-xs gap-0.5">
    <div class="p-2 border border-dotted border-blue">First child</div>
    <div class="p-2 border border-dotted border-green">Second child</div>
    <div class="p-2 border border-dotted border-purple flex-1">Third child</div>
  </div>
</div>
</div>

---
layout: dynamic-image
image: ./images/flexbox.jpg
equal: false
left: false
---

# Flexbox
Allowing flex items to shrink or grow

<Transform scale="0.95">
<div v-click>

```css {*}{lines:true}
.my-flexible-element {
  display: flex;
}
.my-flexible-element .first-element {
  flex-grow: 1; /* Take 1/3 of the free space */
}
.my-flexible-element .third-element {
  flex-grow: 2; /* Takes 2/3 of the free space */
}
```

</div>

<div v-click="2">

```css {*}{lines:true}
.my-flexible-element {
  display: flex;
}
.my-flexible-element .first-element {
  /* Shortend: flex-grow | flex-shrink | flex-basis */
  flex: 1 1 auto;
}
.my-flexible-element .third-element {
  /* Shortend: flex-grow: 2 | flex-shrink: 1 | flex-basis: 0 */
  flex: 2;
}
```

</div>
</Transform>
<div v-motion v-click="1" :initial="{x: 999, y: -999}" :enter="{x: 570, y: -250}" class="absolute w-1/3 p-2 bg-gray-700 text-white dark:text-gray-800 dark:bg-white rounded-md border-2 border-teal-600">
  <div class="p-0.5 flex border border-red text-xs gap-0.5">
    <div class="p-2 border border-dotted border-blue flex-1">First child</div>
    <div class="p-2 border border-dotted border-green">Second child</div>
    <div class="p-2 border border-dotted border-purple flex-[2]">Third child</div>
  </div>
</div>
<div v-click="3" class="-mt-5">More on <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/flex">flex</a></div>

---
layout: dynamic-image
image: ./images/flexbox.jpg
equal: false
left: false
---

# Flexbox
A few games to practice

- [Flexbox Froggy](https://flexboxfroggy.com/)
- [Flexbox Adventure](https://codingfantasy.com/games/flexboxadventure/play)

<img v-motion :initial="{x: 999, y: -999}" :enter="{x: 570, y: -180}" class="absolute rounded-md border-2 border-teal-600 h-56" src="/images/gifs/gaming.webp" alt="Game controller GIF" />

---
layout: dynamic-image
image: ./images/fonts.jpg
equal: false
---

# Custom fonts
Give your text some pizzazz!

Until now you had to use boring fonts only available on the users’device.  
CSS offers a way to embed custom fonts to your website so you can use whatever font you like without asking visitors to download and install it.  
As for videos and audio files, there are multiple formats:

<v-clicks>

- **OTF**: Open Type Font, one of the most known format
- **TTF**: True Type Font, very similar to OTF
- **WOFF** and **WOFF2**: Web Open Format Font, very light format designed for the web (favor them if you can)
- **SVG**: Vectorial font

</v-clicks>

---
layout: dynamic-image
image: ./images/fonts.jpg
equal: false
---

# Custom fonts
Loading your font

You should use different formats for better compatibility.

<div v-click>

### Casting a wide net
```css {*}{lines:true}
@font-face {
  font-family: 'quadranta'; /* Name of the font to use in you code */
  src: url('quadranta.otf') format('truetype'),
    url('quadranta.woff') format('woff'),
    url('quadranta.svg#QuadrantaBold') format('svg');
  font-weight: normal;
  font-style: normal;
}
```

</div>

<div v-click>

### Favor modern formats
```css {*}{lines:true}
@font-face {
    font-family: 'quadranta'; /* Name of the font to use in you code */
    src: url('quadranta.woff2') format('woff2'),
         url('quadranta.woff') format('woff');
    font-weight: normal;
    font-style: normal;
}
```

</div>

---
layout: dynamic-image
image: ./images/fonts.jpg
equal: false
---

# Custom fonts
Loading your font

If the font you want to load is installed on the server where your website is hosted, you can load the font from it first and then fallback to a font file.

<div v-click>

```css {*}{lines:true}
@font-face {
  font-family: MyHelvetica;
  src: local("Helvetica Neue Bold"), /* Look for the font */
      local("HelveticaNeue-Bold"), /* On the local server */
      url('HelveticaNeue-Bold.woff2') format('woff2'),
      url('HelveticaNeue-Bold.woff') format('woff');
  font-weight: bold;
}
```

</div>
<div v-click class="-mt-3">

Finally, use your custom font.
```css {*}{lines:true}
body {
  font-family: 'MyHelvetica';
}
h1 {
  font-family: 'quadranta';
}
```

</div>

---
layout: dynamic-image
image: ./images/fonts.jpg
equal: false
---

# Custom fonts
Finding and generating format files

You can download free fonts form many websites. OTF and TTF will be the most popular formats as you can install them on your operating system.

[FontSquirrel Webfont Generator](https://www.fontsquirrel.com/tools/webfont-generator) will take your OTF or TTF file and generate both WOFF and WOFF2 formats alongside a CSS file containing the code you need to include in your website to load your custom font.

---
layout: dynamic-image
image: ./images/fonts.jpg
equal: false
---

# Custom fonts
Google could already have the answer

A good alternative to spending time downloading fonts, converting them in the right format and write the code needed to include them in your CSS, would be [GoogleFonts](https://fonts.google.com/).

You will be able to embed web fonts in your website in no time, Google handles the files for you and tells you what code you need to insert in the `head` tag.

<img v-click v-motion :initial="{x: 999, y: -999}" :enter="{x: -260, y: -220}" class="absolute rounded-md border-2 border-teal-600 h-56" src="/images/gifs/scrabble.webp" alt="Scrabble type writer GIF" />

---
layout: dynamic-image
image: ./images/pseudo-classes.jpg
equal: false
left: false
---

# Pseudo-classes
And you call yourself a class…

Pseudo-classes are keywords suffixed to CSS selectors. They represent a special state targeted elements might be in at some point.

<div v-click>

```css {*}{lines:true}
.my-element:hover {
  background: red;
  color: white;
}
```

</div>

<ComplementaryMessage type="alert" bordered>Pseudo-classes are not necessarily at the end of a CSS selector. For example, your might want to target descendants of an element in a special state.</ComplementaryMessage>

<div v-click class="mt-4">

```css {*}{lines:true}
.my-element:hover .my-child {
  font-size: 16px;
}
```

</div>

---
layout: dynamic-image
image: ./images/pseudo-classes.jpg
equal: false
left: false
---

# Pseudo-classes
And you call yourself a class…

### Pointer passing over an element
```css {*}{lines:true}
.my-element:hover {
  background: red;
  color: white;
}
```

<div v-motion v-click :initial="{x: 999, y: -999}" :enter="{x: 570, y: -85}" class="absolute w-1/3 p-2 bg-gray-700 text-white dark:text-gray-800 dark:bg-white rounded-md border-2 border-teal-600">
  <div class="p-4 border rounded-md hover:bg-red hover:text-white">
    Try and hover me!
  </div>
</div>

<div v-click>

### Hyperlink pseudo-classes
```css {*}{lines:true}
a:link { /* Links which have not been visited yet */
  color: green;
}
a:visited { /* Links which have been visited */
  color: red;
}
a:hover { /* Hovered links */
  color: transparent;
  background-image: linear-gradient(to right, #ff8177 0%, #ff867a 0%,
     #ff8c7f 21%, #f99185 52%, #cf556c 78%, #b12a5b 100%);
  background-clip: text;
}
```

</div>
<div v-motion v-click :initial="{x: 999, y: -999}" :enter="{x: 570, y: -200}" class="absolute w-1/3 p-2 bg-gray-700 text-white dark:text-gray-800 dark:bg-white rounded-md border-2 border-teal-600">
  <style>
    .link-hover:hover {
      color: transparent !important;
      background-image: linear-gradient(to right, #ff8177 0%, #ff867a 0%,
        #ff8c7f 21%, #f99185 52%, #cf556c 78%, #b12a5b 100%);
      background-clip: text;
    }
  </style>
  <div class="p-4 border rounded-md flex flex-col items-center gap-4">
    <a href="https://google.fr" class="!border-none link:text-green visited:text-red link-hover">I haven’t been visited yet</a>
    <a href="https://lemonde.fr" class="!border-none link:text-green visited:text-red link-hover">I have been visited already</a>
    <a href="https://youtube.fr" class="!border-none link:text-green visited:text-red link-hover">Hover me and my buddies</a>
  </div>
</div>

---
layout: dynamic-image
image: ./images/pseudo-classes.jpg
equal: false
left: false
---

# Pseudo-classes
And you call yourself a class…

### Combining pseudo-classes
```css {*}{lines:true}
table tr:not(:last-child) {
  /* Targets every <tr> tags except for the last of the <table> */
  border-bottom: 1px solid blue;
}
```

<div v-motion v-click="[1,2]" :initial="{x: 999, y: -999}" :enter="{x: 570, y: -170}" class="absolute w-1/3 p-2 bg-gray-700 text-white dark:text-gray-800 dark:bg-white rounded-md border-2 border-teal-600">
  <table class="!border-none">
    <tr class="border-bottom !border-blue">
      <th>Title 1</th>
      <th>Title 2</th>
    </tr>
    <tr class="border-bottom !border-blue">
      <td >Value 1</td>
      <td>Value 2</td>
    </tr>
    <tr class="border-bottom !border-blue">
      <td>Value 1</td>
      <td>Value 2</td>
    </tr>
    <tr class="border-none">
      <td>Value 1</td>
      <td>Value 2</td>
    </tr>
  </table>
</div>

<div v-click="2">

### Using special keywords
```css {*}{lines:true}
table tr:nth-child(even){ /* Every even <tr> */
  background: green;
}
table tr:nth-child(odd){ /* Every odd <tr> */
  background: red;
}
```

</div>

<div v-motion v-click="3" :initial="{x: 999, y: -999}" :enter="{x: 570, y: -235}" class="absolute w-1/3 p-2 bg-gray-700 text-white dark:text-gray-800 dark:bg-white rounded-md border-2 border-teal-600">
  <table class="!border-none">
    <tr class="!border-none bg-red">
      <th>Title 1</th>
      <th>Title 2</th>
    </tr>
    <tr class="!border-none bg-green">
      <td >Value 1</td>
      <td>Value 2</td>
    </tr>
    <tr class="!border-none bg-red">
      <td>Value 1</td>
      <td>Value 2</td>
    </tr>
    <tr class="!border-none bg-green">
      <td>Value 1</td>
      <td>Value 2</td>
    </tr>
  </table>
</div>
<div v-click="4">

More on [pseudo-classes](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes)

</div>

---
layout: dynamic-image
image: ./images/pseudo-elements.jpg
equal: false
---

# Pseudo-elements
You’ll fit right in

Pseudo-elements select a part of the targeted element. Some pseudo-elements create a new inline child element.

<div v-click>

```css {*}{lines:true}
.my-element::first-line {
  color: red;
}
```

</div>
<div v-motion v-click :initial="{x: 999, y: -999}" :enter="{x: -360, y: -215}" class="absolute w-1/3 p-2 bg-gray-700 text-white dark:text-gray-800 dark:bg-white rounded-md border-2 border-teal-600">
  <p class="text-xs first-line:text-red">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Praesent ornare ligula sem, nec dapibus nisl cursus sagittis. Cras pharetra sit amet tortor sit amet consectetur. In hac habitasse platea dictumst. Cras sed tortor leo. Quisque fringilla gravida finibus. Nunc in scelerisque neque. Nam elementum luctus molestie. Donec suscipit aliquet lacus ut mattis.</p>
</div>

<ComplementaryMessage bordered>Notice the double colon <strong>::</strong> compared to pseudo-classes which have simple colon <strong>:</strong></ComplementaryMessage>

---
layout: dynamic-image
image: ./images/pseudo-elements.jpg
equal: false
---

# Pseudo-elements
You’ll fit right in

### Pseudo-elements that create new descendant
```css {*}{lines:true}
li::before {
  content: '🎁';
}
li::after {
  content: '✅';
}
```

<div v-motion v-click :initial="{x: 999, y: -999}" :enter="{x: -360, y: -125}" class="absolute w-1/3 p-2 bg-gray-700 text-white dark:text-gray-800 dark:bg-white rounded-md border-2 border-teal-600">
  <ul class="list-none">
    <li class="list-none before:content-['🎁'] after:content-['✅']">My item 1</li>
    <li class="list-none before:content-['🎁'] after:content-['✅']">My item 2</li>
    <li class="list-none before:content-['🎁'] after:content-['✅']">My item 3</li>
  </ul>
</div>
<div v-click>

More on [pseudo-elements](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-elements)

</div>

---
layout: dynamic-image
image: ./images/screens.jpg
equal: false
left: false
---

# Media queries
It’s time to adapt to the media

Media queries define CSS rules only applied to certain media with sepcific conditions: their type, their size, their orientation, etc.

There are two way to apply media queries to a website:

<v-clicks>

- Creating a new CSS file and insert it via a `link` tag and setting the conditions with a `media` attribute
- Inserting media queries directly into the CSS code

</v-clicks>

---
layout: dynamic-image
image: ./images/screens.jpg
equal: false
left: false
---

# Media queries
It’s time to adapt to the media

### Inserting a new CSS file with media conditions
```html {*}{lines:true}
<!-- Remember, this goes inside the <head> tag -->
<link rel="stylesheet" media="screen and (max-width: 640px)" 
  href="smallscreen.css" type="text/css" />
```

### Media queries inside a CSS file
```css {*}{lines:true}
/* CSS for media of type "screen" with a maximum width of 640px */
@media screen and (max-width: 640px){
  .my-new-block {
    display:block;
  }
}
```

<ComplementaryMessage type="alert" bordered>Pick one method, you don’t need to do both.</ComplementaryMessage>

---
layout: dynamic-image
image: ./images/screens.jpg
equal: false
left: false
---

# Media queries
It’s time to adapt to the media

### Types of media
- **screen**: all devices which are considered as screens (computer, tablet, phone, tv, projector, etc.)
- **print**: printing media
- **all**: all of the above, which is the default behavior when applying CSS rules

---
layout: dynamic-image
image: ./images/screens.jpg
equal: false
left: false
---

# Media queries
It’s time to adapt to the media

### Using some common conditions
```css {*}{lines:true}
/* Screens with a minimum width of 1024px and a maximum of 1280px */
@media screen and (min-width: 1024px) and (max-width: 1280px) {
  .wide {
    background: #000;
    color: #fff;
  }
}
```
```css {*}{lines:true}
/* Screens which are in portrait mode */
@media screen and (orientation: portrait) {
  .portrait {
    background:#000;
    color: #fff;
  }
}
```

<div v-click>

More on [media queries](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_media_queries/Using_media_queries)

</div>

---
layout: intro
image: ./images/thinker.jpg
---

<div class="absolute inset-0 flex justify-center items-center">
  <h1 class="text-6xl !text-white font-500">Questions?</h1>
</div>

<div class="absolute bottom-4 right-4 opacity-50 text-sm italic">
  © Unsplash<br>© Giphy
</div>
