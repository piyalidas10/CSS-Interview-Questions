# CSS-Interview-Questions

### 1. What is CSS and what are its key features?

<details><summary><b>Answer</b></summary>
<p>

#### 
CSS is a style sheet programming language that helps configure and manage the appearance and formatting of a document created in a markup language. It gives HTML (Hypertext Markup Language) an extra feature. It's typically combined with HTML to modify the look and feel of web pages and user interfaces.
https://pwskills.com/blog/features-of-css/

</p>
</details>

---

### 2. Explain the difference between margin and padding.

<details><summary><b>Answer</b></summary>
<p>

#### 
Margin is the space outside of the component's edge or border. Padding is the space inside of the component's edge or border. It is possible to set the margin to auto.

</p>
</details>

---

### 3. How does the box model work in CSS?

<details><summary><b>Answer</b></summary>
<p>

#### 
The CSS Box Model is a layout model that describes how different components of a web element (content, padding, border, and margin) are structured and positioned. Each web element generates a rectangular box that encompasses these components, and the Box Model allows developers to control the element’s size and spacing effectively.

The components of the CSS Box Model are:

Content: The actual content of the box, such as text or an image.
Padding: The space between the content and the border.
Border: The edge surrounding the padding and content.
Margin: The space outside the border, separating the element from other elements.

</p>
</details>

---

### 4. Describe the concept of specificity in CSS.

<details><summary><b>Answer</b></summary>
<p>

#### 
CSS Specificity is a fundamental concept in CSS that determines the order of style application. It is calculated based on the types of selectors used, including inline styles, IDs, classes, attributes, and element types. 

Understanding CSS Specificity is important for:
Avoiding styling conflicts
Ensuring consistent design application
Maintaining control over CSS code

| Priority                     | Description                                                                                                                                                       |
| ---------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Inline style                 |  Highest priority, directly applied using the style attribute.
| ID selectors                 |  Second highest priority, identified by the unique id attribute of an element.
| Classes, pseudo-classes,     |  Medium level of specificity, targeted using class names, pseudo-classes like :hover, and
| attributes                   |  attributes like [type="text"].
| Elements and pseudo-elements |  Lowest priority, applies to HTML elements and pseudo-elements such as ::before and ::after.

</p>
</details>

---

### 5. Explain the difference between inline, block, and inline-block elements.

<details><summary><b>Answer</b></summary>
<p>

#### 
inline : The element doesn’t start on a new line and only occupy just the width it requires. You can’t set the width or height. Any height and width properties will have no effect. Here are a few elements that have a default inline property: span, a, img, em, strong, i, small
```
.inline-element {
  display: inline;
  width: 1000px; /* ❌ won't have any effect */
  height: 1000px; /* ❌ won't have any effect */
}
```

inline-block: It’s formatted just like the inline element, where it doesn’t start on a new line. BUT, you can set width and height values.
```
.inline-block-element {
  display: inline-block;
  width: 1000px; /* ✅  yes, it will work */
  height: 1000px; /* ✅  yes, it will work */
}
```

Block : block starts on a NEW line and takes up the full width available. So that means block elements will occupy the entire width of its parent element. And you can set width and height values. Here are a few elements that have a default block property: div, h1, p, li, section etc.

-------------------------------------------------------------------------------------------------------------------
Block elements: They consume the entire width available irrespective of their sufficiency. They always start in a new line and have top and bottom margins. It does not contain any other elements next to it.

Examples of Block elements:

<h1>-<h6> : This element is used for including headings of different sizes ranging from 1 to 6.
<div>: This is a container tag and is used to make separate divisions of content on the web page.
<hr>: This is an empty tag and is used for separating content by horizontal lines.
<li>: This tag is used for including list items of an ordered or unordered list.
<ul>: This tag is used to make an unordered list.
<ol>: This tag is used to make an ordered list.
<p>: This tag is used to include paragraphs of content in the webpage.
<table>: This tag is used for including the tables in the webpage when there is a need for tabular data.

Inline elements: Inline elements occupy only enough width that is sufficient to it and allows other elements next to it which are inline. Inline elements don’t start from a new line and don’t have top and bottom margins as block elements have.

Examples of Inline elements:

<a>: This tag is used for including hyperlinks in the webpage.
<br>: This tag is used for mentioning line breaks in the webpage wherever needed.
<script> : This tag is used for including external and internal JavaScript codes.
<input>: This tag is used for taking input from the users and is mainly used in forms.
<img>: This tag is used for including different images in the webpage to add beauty to the webpage.
<span>:  This is an inline container that takes necessary space only.
<b>:  This tag is used in places where bold text is needed.
<label>: The tag in HTML is used to provide a usability improvement for mouse users i.e, if a user clicks on the text within the <label> element, it toggles the control.

</p>
</details>

---

### 6. What are pseudo-classes and pseudo-elements in CSS?

<details><summary><b>Answer</b></summary>
<p>

#### 
Pseudo-classes and pseudo-elements in CSS are selectors that allow the styling of specific states or parts of elements.

Pseudo-classes : 
Style an element when a user moves the mouse over it
Style visited and unvisited links differently
Style an element when it gets focus
Style valid/invalid/required/optional form elements

Pseudo-elements :
Style the first letter or line, of an element
Insert content before or after an element
Style the markers of list items
Style the viewbox behind a dialog box

</p>
</details>

---

### 7. How do you center elements horizontally and vertically in CSS?

<details><summary><b>Answer</b></summary>
<p>

#### 
Using flexbox
```
<div class="container">
  <div class="item">I am centered!</div>
</div>

div {
  border: solid 3px;
  padding: 1em;
  max-width: 75%;
}

.item {
  border: 2px solid rgb(95 97 110);
  border-radius: 0.5em;
  padding: 20px;
  width: 10em;
}

.container {
  height: 8em;
  border: 2px solid rgb(75 70 74);
  border-radius: 0.5em;
  font: 1.2em sans-serif;

  display: flex;
  align-items: center;
  justify-content: center;
}
```

Using grid
```
<div class="container">
  <div class="item">I am centered!</div>
</div>

div {
  border: solid 3px;
  padding: 1em;
  max-width: 75%;
}

.item {
  border: 2px solid rgb(95 97 110);
  border-radius: 0.5em;
  padding: 20px;
  width: 10em;
}

.container {
  height: 8em;
  border: 2px solid rgb(75 70 74);
  border-radius: 0.5em;
  font: 1.2em sans-serif;

  display: grid;
  place-items: center;
}
```

Position: Absolute and Transform: Translate
```
<div class="container">
  <div>I am centered!</div>
</div>
.container {
  position: relative;
  height: 100vh;
}

div {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 50%;
  height: 50%;
}
```

Table and Table-Cell
```
<div class="container">
  <div>I am centered!</div>
</div>

.container {
  display: table;
  height: 100vh;
  width: 100%;
}
div {
  display: table-cell;
  vertical-align: middle;
  text-align: center;
  width: 50%;
  height: 50%;
}
```

Line-Height
```
<div class="container">
  <div>I am centered!</div>
</div>

.container {
  height: 100vh;
  width: 100%;
  text-align: center;
}
div {
  display: inline-block;
  line-height: 100vh;
  vertical-align: middle;
  width: 50%;
  height: 50%;
}
```
  
</p>
</details>

---

### 8. What is the difference between display: none and visibility: hidden?

<details><summary><b>Answer</b></summary>
<p>

#### 
"display: none" and "visibility: hidden" are two CSS properties used to control the visibility of elements on a webpage. "display: none" removes the element from the layout, while "visibility: hidden" hides the element while preserving its position.

</p>
</details>

---

### 9. Describe the difference between position: relative, position: absolute, and position: fixed.

<details><summary><b>Answer</b></summary>
<p>

#### 
Relative Positioning is a CSS technique that allows an element to be adjusted from its normal position. The syntax for relative positioning is position: relative; When you set the top, right, bottom, and left properties of an element with relative positioning, it moves from its original location.
  
Absolute Position is another CSS technique that adjusts an element’s position relative to its parent. If no parent element is present, the document body is used as the parent.

Fixed Position is a CSS technique that keeps an element in the same place even when the page is scrolled. The syntax for fixed positioning is position: fixed;. To position the element, we use top, right, bottom, and left properties.
  
https://www.geeksforgeeks.org/difference-between-relative-and-absolute-position-in-css/

</p>
</details>

---

### 10. How do you implement responsive design in CSS?

<details><summary><b>Answer</b></summary>
<p>

#### 


</p>
</details>

---

### 11. What are CSS selectors and how do you use them?

<details><summary><b>Answer</b></summary>
<p>

#### 


</p>
</details>

---

### 12. Explain the concept of the CSS box-sizing property.

<details><summary><b>Answer</b></summary>
<p>

#### 


</p>
</details>

---

### 13. Describe the difference between flexbox and grid layout.

<details><summary><b>Answer</b></summary>
<p>

#### 


</p>
</details>

---

### 14. How do you handle browser compatibility issues in CSS?

<details><summary><b>Answer</b></summary>
<p>

#### 


</p>
</details>

---

### 15. What is the purpose of the z-index property in CSS?

<details><summary><b>Answer</b></summary>
<p>

#### 


</p>
</details>

---

### 16. Explain the concept of CSS transitions and animations.

<details><summary><b>Answer</b></summary>
<p>

#### 


</p>
</details>

---

### 17. How do you vertically align text in CSS?

<details><summary><b>Answer</b></summary>
<p>

#### 


</p>
</details>

---

### 18. Describe the difference between em and rem units in CSS.

<details><summary><b>Answer</b></summary>
<p>

#### 


</p>
</details>

---

### 19. What is the clearfix hack and when is it used?

<details><summary><b>Answer</b></summary>
<p>

#### 


</p>
</details>

---

### 20. How can you optimize CSS for performance?

<details><summary><b>Answer</b></summary>
<p>

#### 


</p>
</details>

---

### 21. What are CSS floats and how do they work?

<details><summary><b>Answer</b></summary>
<p>

#### 


</p>
</details>

---

### 22. Explain the concept of CSS specificity.

<details><summary><b>Answer</b></summary>
<p>

#### 


</p>
</details>

---

### 23. How do you implement a sticky footer in CSS?

<details><summary><b>Answer</b></summary>
<p>

#### 


</p>
</details>

---

### 25. What is the purpose of the CSS transform property?

<details><summary><b>Answer</b></summary>
<p>

#### 


</p>
</details>

---

### 26. How do you create CSS sprites and why are they used?

<details><summary><b>Answer</b></summary>
<p>

#### 


</p>
</details>

---

### 27. Explain the concept of CSS preprocessors like SASS and LESS.

<details><summary><b>Answer</b></summary>
<p>

#### 


</p>
</details>

---

### 28. Describe the difference between margin collapsing and margin collapsing prevention.

<details><summary><b>Answer</b></summary>
<p>

#### 


</p>
</details>

---

### 29. How do you handle vendor prefixes in CSS?

<details><summary><b>Answer</b></summary>
<p>

#### 


</p>
</details>

---

### 30. What are the advantages and disadvantages of using CSS frameworks like Bootstrap?

<details><summary><b>Answer</b></summary>
<p>

#### 


</p>
</details>

---



