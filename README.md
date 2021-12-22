# Udemy-Progress-Updater
It will help you complete/reset your Udemy course in 1 tap.

## Just follow below steps for complete or reset your udemy course.

1. Open udemy course with Course content (sidebar on right).
2. Right click on browser and open `Inspect` or press `ctrl+shift+i` and click on `console`

### To Complete your Progress

Open all the sections in course content you wanna complete and paste below code in console and press `Enter`

```js
const sectionEl = document.querySelectorAll("div[aria-expanded='false']");
const checkboxes = document.querySelectorAll("input[type='checkbox']");
checkboxes.forEach((checkbox) => {
  if(!checkbox.checked) {
    checkbox.click();
  }
})
```

### To Reset your Progress

Open all the sections in course content you wanna reset and paste below code in console and press `Enter`

```js
const sectionEl = document.querySelectorAll("div[aria-expanded='false']");
const checkboxes = document.querySelectorAll("input[type='checkbox']");
checkboxes.forEach((checkbox) => {
  if(checkbox.checked) {
    checkbox.click();
  }
})
```

Note: Most probably it is not gonna reset your progress which is showing on header. This hack was for completing/resetting viewed lectures.
