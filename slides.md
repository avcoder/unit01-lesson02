---
# You can also start simply with 'default'
theme: default
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: /assets/intro.jpg
# some information about your slides (markdown enabled)
title: Software Development | Foundations
info: |
  ## Software Development | Foundations
# apply unocss classes to the current slide
class: text-left
drawings:
  persist: false
transition: slide-left
mdc: true
---

# HTML - part 2
Software Development Bootcamp - Circuit Stream
- [ ] Remember concepts from previous lesson
- [ ] HTML5, DOCTYPE tag etc, attributes, 
- [ ] HTML Layout Elements

<div class="abs-br m-6 text-xl">
  <a href="https://github.com/slidevjs/slidev" target="_blank" class="slidev-icon-btn">
    <carbon:logo-github />
  </a>
</div>

<!--
TODO: fill in anchor href above to point to github repo for these slides
- take attendance
- verify previous zoom video uploaded
-->

---
transition: slide-left
---

# Q&A
(5 min)

- 🪲 Stuck on a bug?  Chat with me Discord avcoder1274.  Or #troubleshoot-forum.  Or DM each other.
- 🌐 Where to Host Personal Website? Will show you eventually (ensure you made a Github account)
- 👻 What happens if I'm not able to make it to class?
- 🆎 Closed captioning available on zoom (refer to [youtube link](https://www.youtube.com/watch?v=xN_wLFIz1K0) to hide/show it)
- 🖱️ My slide links: can also open via Shift + click


<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

<!--
Q: miss class? 
A: Totally understandable.  I'm okay if you can't make it for the whole 2.5 hours; I'm okay if you attend just part of the class since you have a 3 year old and are in Brazil. Just make sure to DM me so I can mark you present.  If you totally miss a class that's okay too as long as you watch the videos to keep up.  If you miss many classes because of life circumstances, I understand, but I'm obliged to inform Circuit Stream of any total absences which might alert them to contact you to ask if everything is alright.  And yes, I do take attendance every class.
-->

---
transition: slide-left
---

# Summary from Last Class
(5 min)

- 🏃‍♀️‍➡️ **Important to practice software development** 
- ⛳ What do most HTML tags have in common (i.e. syntax)?
- 🖱️ How can you see the HTML when viewing a webpage?
- 🌐 What main website can be used as a reference to check how an HTML tag is used?
- ✅ What website can be used to check if your HTML is valid?
- 📂 Traditionally, the URL path is equivalent to the [path](http://www.mixed-up.com/cs/community/) to your folder/file

Did you know you can [check](https://caniuse.com/) if a particular HTML/CSS/JS feature is implemented in all browsers?

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

<!--
- Satisfy your curiosities (what happens if I do this?)
- Get used to: coding, syntax, paying attention to details, problem-solving via logical thinking
- Visual feedback of HTML is good for learners
- web app vs web site (not every site is client generated. Most are still server generated)
-->

---
transition: slide-left
---

# Web Standards Key Principles
(5 min)

- [MDN link](https://developer.mozilla.org/en-US/docs/Learn_web_development/Getting_started/Web_standards/The_web_standards_model#web_standards_key_principles) for key principles

|                                                     |                             |
| --------------------------------------------------- | --------------------------- |
| "Open" standards                 | free to contribute and use. No patents     |
| Accessible | access to info to people with disabilities, regardless of circumstance |
| Interoperable                        | websites should consistently work across multiple browsers              |
| Don't break the web                                     | new tech should be backwards compatible                 |

<!-- 
1. Open: no one company controls web.  ex: Flash vs. Apple
2. Accessible: navigate via keyboard.  Screen readers.  Lighthouse tab.
3. Interoperable: browsers should render same output given same input
4. Don't break web: browser vendors should implment new web tech without causing a difference in rendering or functionality
-->

---
transition: slide-left
---

# Tech Stack of the Web
(5 min)

|                                                     |                             |
| --------------------------------------------------- | --------------------------- |
| 📬 HTTP | communication protocol of the web between your browser and server |
| 🩻 HTML | structure and meaning (semantics)     |
| 👔 CSS | styling and layout |
| ⛹️‍♂️ JavaScript      | controlling dynamic behaviour              |
| 🖼️ Frameworks      | you'll learn [React](https://react.dev/), [node.js](https://nodejs.org/en), [express](https://expressjs.com/), [Vite](https://vite.dev/), [mongoDB](https://www.mongodb.com/), [mongoose](https://mongoosejs.com/)      |
| 🎨 Browsers | Chrome, Firefox, Safari |

<!-- 
1. HTTP: like sending a letter thru mailbox. Hypertext Transfer Protocol.
2. HTML: semantics. ex: screen reader use semantic HTML. w3c validator
3. CSS: cosmetic. ex: cssgarden
4. JS: logic, fetching data, 
5. Frameworks: updates UI to reflect state 
6. Browsers Engine: Chromium/Blink (Edge, Opera, Brave). WebKit (Safari). Gecko (Firefox)
-->

---
transition: slide-left
---

# Basic HTML document
(15 min)

```html
<!DOCTYPE html>
<html lang="en"> <!-- Inspect https://horecamenu.pl/ -->
<head>
    <meta charset="UTF-8"> <!-- Try "ISO-8859-1" -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0"> <!-- Try removing content with  circuitstream.com -->
    <title>Document</title>
    <style>
      /* styles can go here */
    </style>
    <script src="index.js"></script>
</head>
<body>
    <p>This page contains special characters: ñ, é, ü</p>
</body>
</html>
```

<!--
- DOCTYPE - specifies which HTML version this document was written in. Without it, browser might default to quirks mode, causing issues in styling or tags not rendering correctly.  All HTML docs should start with this.
- html - encapsulates everything, tells browser to interpret as html. lang attribute specifies language
- UTF-8 - what character encoding is used so that browser knows how to display characters
- viewport - to control layout and zooming of page on mobile devices. Without it, mobile views zoom out
- title tag - try changing it what happens to browser tab?
- style tag - inline css
- script tag - js
- body tag - contains all visible content on page
-->

---
transition: slide-left
---

# Exercise: Create HTML for...
(15 min)

<img src="/assets/cdntire1.png">
<br />

   1. "Shop Now" is an anchor tag (not a button).  Make it go to any shopping website on click
   2. Use `<img>` tag for the picture.  Download by clicking <a href="/assets/patio.png">here,</a>  then right click the image and "Save Image As"
   3. Visualize everything as boxes; this will help you with the container tags go.  
   ex: Below the `<title>` tag, temporarily insert `<style>* {border: 1px solid orange}</style>`

<!-- 
1.
-->

---
transition: slide-left
---

# 10 minute break
<br/>

🍦 Cool Tips, Trends and Resources:
- 📗 [Front End Developer/Engineer Handbook 2024](https://frontendmasters.com/guides/front-end-handbook/2024/?utm_source=boost&utm_medium=blog&utm_campaign=boost)
- 🪙 [HTML5 Boilerplate](https://html5boilerplate.com/) 
- ☑️ [How to use Emmet in VS Code](https://code.visualstudio.com/docs/editor/emmet)
- 🍱 [How to Section Your HTML](https://css-tricks.com/how-to-section-your-html/)
- 🔗 [When to use Buttons vs Links](https://css-tricks.com/a-complete-guide-to-links-and-buttons/)
- 🐙 [Blob Generator](https://www.blobmaker.app/)

---
transition: slide-left
---

# Inline vs Block elements
(5 min)

- By default, the browser stacks elements:
   - top to bottom if block elements
   - left to right if inline elements

See https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_display/Block_and_inline_layout_in_normal_flow

<!--
-->


---
transition: slide-left
---

# The id Attribute
(5 min)

|                                                     |                             |
| --------------------------------------------------- | --------------------------- |
| 📬 Uniquely identify tags | `id` must be unique across entire document |
| ⛹️‍♂️ Anchor Link      | can jump to specific sections of page             |
| 🩻 Target tag via CSS | apply styling to particular tag     |
| 👔 Reference tag in JS | allows JS to easily manipulate element |


<!--

Goto: https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/id

2. Goto MDN page and append `#syntax` to url
   - Demo anchor tag (href id on same page, different page)

3. Add `background-color: green`

4. syntax.textContent = "hello world"
syntax.addEventListener('click', () => alert('hello world'))
-->

---
transition: slide-left
---

# Exercise: Create HTML for the nav menu
(15 min)

<img src="/assets/cdntire2.png">
<br />

   1. Goto any website that has similar navigation menus like the one above
   2. What HTML tags do they use to create the navigation menu?
   3. Make each menu, upon clicking it go to another anchor tag, another page, google.ca

<!-- 
1.
-->

---
transition: slide-left
---

# Exercise
(30 min) Group exercise <a href="/assets/mockup.png">Click here to see Mockup</a>

1. Create an HTML document with the menu for a restaurant (see next slide for text)
   - There are 3 major sections: Plates, Drinks, Desserts
   - Each section includes 3 food items
   - Each food item shows heading, description, price, picture, Add to Order button
2. Create a nav menu up top with 3 items: Plates, Drinks, Desserts
3. Clicking nav menu item Plates should scroll down to correct position of Plates section
4. For the images, may use temporary placeholder images via

`<img src="https://placehold.co/300x200?text=Pretend+Chicken" alt="pretend chicken">`

Stretch Goals if you have time:
- Open a new tab, and enter the image placeholder link above.  Inspect it -- what tag is it using?
- Replace all placeholder images with actual images.  Feel free to Cmd+Shift+4 food images on the internet, save them locally alongside your index.html, then refer to it in your image's `src`

---
transition: slide-left
---

```
Menu

Plates
Plate 1: Grilled Chicken - Tender chicken breast seasoned and grilled to perfection. 
 Price: $12.99
Plate 2: Spaghetti Bolognese - Classic Italian dish with hearty meat sauce served over spaghetti.
 Price: $14.99
Plate 3: Vegetarian Stir-Fry - Fresh mixed vegetables stir-fried in a savory sauce.
 Price: $10.99

Drinks
Drink 1: Fresh Orange Juice - Refreshing and freshly squeezed orange juice.
 Price: $4.99
Drink 2: Classic Mojito - A refreshing blend of mint, lime, and soda with a touch of sweetness.
 Price: $8.99
Drink 3: Iced Cappuccino - Chilled cappuccino with a shot of espresso, milk, and ice.
 Price: $6.99

Desserts
Dessert 1: Chocolate Cake - Rich and moist chocolate cake topped with velvety chocolate frosting.
 Price: $7.99
Dessert 2: Tiramisu - Classic Italian dessert with layers of coffee-soaked ladyfingers and mascarpone cream.
 Price: $9.99
Dessert 3: Fruit Tart - Fresh fruit medley on a delicate pastry crust with a light glaze.
 Price: $8.99
```

<!--
-->

---
transition: slide-left
---

# Compare your HTML to Canadian Tire's
(5 min)

- Goto https://www.canadiantire.ca/en.html
- Compare nav menu and (scroll down) "Patio trends & inspiration 2025" with bare HTML
- Inspect page, delete `<head>`

---
transition: slide-left
---

# HTML Layouts
(5 min)

- See https://www.w3schools.com/html/html_layout.asp
- CSS containers: these layout elements will be used with css files in next class

## For homework:
- put your menu sections inside the containers tags
- Practice with the exercise that is in LMS "Build a basic page that includes info about your fav musician, their skills, and pics/videos (this is not graded, but good for practice)

<!--
-->

---
transition: slide-left
---

# Git, Github and deployment 
(if we have time)

- Follow along on how to use git, Github, and deploy your site

<!--
-->

---
transition: slide-left
---