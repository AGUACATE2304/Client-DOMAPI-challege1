# Introduction to DOM - Exercises

1. Answer the following questions:

   - How would you select from JavaScript an element `p` that has the class `text` and also the class `important`?
   - `document.querySelector('.text.important');`
   - How would you select from JavaScript a `button` element with class `button` and that is disabled?
   -`document.querySelector('.button');`
   - How would you select from JavaScript all the `li` elements that are direct children of an `ul` element with class `list`?
   - `document.querySelectorAll('.list');`
   - How would you select from JavaScript all the `input` elements that are descendants of a `form` element with class `form-new-item`, and that have a `type` attribute with a value `text`?
   - `document.querySelectorAll('form.form-new-item input[type="text"]');`

2. From the following HTML structure, create a script that selects the header "The MEAN stack". Next, change the text to "The MERN stack" and remove the "subtitle" class.

```html
<main class="main-content">
  <h1 class="app-title">Bootcamp technologies</h1>
  <section class="info">
    <h2 class="subtitle">The MEAN stack</h2>
    <p class="text">
      The MEAN stack is the set of technologies used in the bootcamp by
      FullStack Web Development.
    </p>
  </section>
</main>
```
- `Result Script nº2`

```
  const headerSelector = document.querySelector('h2');
  
  headerSelector.innerHTML = "The MERN stack";

  headerSelector.classList.remove("subtitle");

```


3. Here you have an HTML without data:

```html
<article class="student">
  <h2 class="student-name"></h2>
  <span class="student-age"></span> years
  <img class="student-photo" src="" alt="" />
</article>
```

Create a script where you declare a variable with a student's data
(name, age and photo URL). Next, get the elements from the HTML
and fill them in with the student's information.

- `Result Script nº3`

```
const studentName = "Alan Castillo";
const studentAge = 20;
const studentPhotoURL = "https://www.google.com";

const studentNameElement = document.querySelector('.student-name');
const studentAgeElement = document.querySelector('.student-age');
const studentPhotoElement = document.querySelector('.student-photo');

studentNameElement.innerHTML = studentName;
studentAgeElement.textContent = studentAge;
studentPhotoElement.src = studentPhotoURL;
studentPhotoElement.alt = studentName;
  

```