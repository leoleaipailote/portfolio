[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/SdhxV-VK)
# COSC415 Homework 1: HTML/CSS

Due: Tuesday 5 September, 2023, 5pm

---

## Instructions

### Overview

In this homework you'll gain some familiarity and practice with HTML and CSS.  

In the repo, you will find two files --- `index.html` and `site.css` --- that can be used to write the page code and contents.  For any images or additional files used on your page, please just add them to the repo.

Your page can be about either (a) yourself, or (b) something you are interested in.

Guidelines and expectations are listed below.  When you are finished, commit and push your work to Github.

### Testing (style checking)

There is a detailed rubric below on what is expected in your HTML and CSS.  

A key requirement is to adhere to good style in your HTML and CSS for this assignment.  When you push your repo to Github various automated style checking tests will be run on your repo.  In particular [htmlhint](https://htmlhint.com) and [stylelint](https://stylelint.io) will be run.  If you would like to run these tools locally before pushing to Github (recommended), you can do the following:

* On macOS: `brew install npm`
* on Windows WSL/Ubuntu: `sudo apt install npm`

Then (on either OS):

```bash
$ npm install
$ npx stylelint *.css
$ npx htmlhint
```

(There is a `stylecheck.sh` file included in the repo to run both `stylelint` and `htmlhint` using the commands above; you can run it with `./stylecheck.sh`.)

You should have _zero_ errors flagged by these tools when you are complete.

## Guidelines

 * You can use bootstrap css if you'd like, but your `site.css` file must include some significant styling.  Don't just rely on bootstrap.

 * Your page must have at least one HTML table.

 * Your page must have at least one inline image, with an alternative rendering  (alt property).

 * Your page must have structural elements like a header, footer, and main area (and optionally, a sidebar).  The layout for those elements needs to be done through CSS.  You should use `<header>` etc. elements where it makes sense to do so; it is also ok to use `<div>` to more generically identify structural components on your page, but your HTML structure must clearly reflect document structure.

 * Your page must include some kind of non-simplistic (non-default) layout.  For example, you could create a sidebar for navigation, or a fixed position menu along the top of the page.  You'll need to use position directive(s) in CSS in some way to fulfill this requirement.

 * You must use at least two non-default fonts.  You can use webfonts if you want, e.g., https://fonts.google.com or https://fontawesome.com.

 * You must adhere to the principle of "separation of concerns": your HTML should not embed any CSS (apart from a `link` element that references the associated CSS file(s)).

 * You must use at least one CSS class selector, at least one id selector, and at least one "descendent relationship" selector to connect your HTML with appropriate styling.  For example, `tr .data` is a selector that would select any elements with class `.data` nested within a `tr` element.  You may also use a parent (direct descendant) selector (e.g., `tr > .data`)

Overall, your goal is to make a page that you'd be proud to show others, with some modest complexity in its layout and styling.

---

### Detailed rubric

 - Required HTML structural elements are present
   - 0: nothing done
   - 1: No HTML structural elements present beyond `html`, `body`, `head`
   - 2: Generic structural elements are present, e.g., `div`, used in a minimal way
   - 3: Generic (`div`) and some additional structural elements are present to convey document structcure
   - 4: Good use of structural elements to clearly convey semantics of page content

 - Overall layout and visual aspects are styled through CSS 
   - 0: nothing done
   - 1: Some styling of the page through inline styling in HTML; styling directives have clear redundancies; styling directives do not clearly convey styling intent.
   - 2: Layout and visual aspects are styled *only* through CSS (no styling embedded in HTML); some redundancy in styling is present; styling directives do not always convey styling intent, e.g., by using poor names.
   - 3: Layout and visual aspects are styled *only* through CSS; minimal redundancy is present in CSS directives; CSS directives mostly convey styling intent through use of good names, etc.
   - 4: Layout and visual aspects are styled *only* through CSS; no unnecessary redundancy is present in CSS; CSS directives are correct and clearly expressed, with CSS expressions clearly conveying styling intent.

 - Use of a non-simplistic layout using position CSS directive
   - 0: nothing done
   - 1: CSS positioning directives are incorrect or do not render correctly.
   - 2: CSS positioning directives are present, but do not alter the default rendering position.
   - 3: Use of CSS positioning directives are correct and place one or more elements in non-default positions, but may not render correctly (e.g., element spills off the screen).
   - 4: Use of CSS positioning directives are correct, render correctly, and place one or more elements in non-default positions.

 - HTML table present
   - 0: nothing done
   - 1: HTML table is present, but no rows or data.
   - 2: HTML table is present in the most minimal way, e.g., single row or single column.
   - 3: HTML table is present but headers, structure, or content are trivial or minimal.
   - 4: HTML table is present with well-constructed headers, structure, and content.

 - Inline image is present
   - 0: nothing done
   - 1: Image tag is present but broken.
   - 2: Image tag is present, but image is rendered poorly (e.g., aspect ratio is warped) and/or alt property is not present.
   - 3: Image tag is present and image renders properly, but alt does not convey meaningful information.
   - 4: Image tag is present, alt is present and conveys something meaningful about the image, image renders correctly and as intended, caption may also be present.

 - Use of at least two non-default fonts
   - 0: nothing done
   - 1: only default fonts are used
   - 2: non-default fonts are included (e.g., `link` element present) but are not actually used
   - 3: one non-default font is used in addition to default fonts
   - 4: at least two non-default fonts are used in addition to default fonts

 - Use of at least one CSS class selector
   - 0: nothing done
   - 1: CSS class selector is present in CSS file, but not used in HTML
   - 2: CSS class selector is present in CSS file, but incorrectly used in HTML
   - 3: CSS class selector is used, but only for a single tag type
   - 4: CSS class selector is effectively used to style elements of different tags

 - Use of at least one CSS id selector
   - 0: nothing done
   - 1: CSS id selector is present in CSS file, but not used in HTML (nothing selected)
   - 2: CSS id selector is present in CSS file, but incorrectly used in HTML (e.g., more than one element uses same id)
   - 3: CSS id selector is used, but only for a single tag type
   - 4: CSS id selector is effectively used to style elements of different tags

 - Use of at least one CSS descendent relationship selector, e.g., `tr .data` (to select elements with class `.data` nested within `tr` elements)
   - 0: nothing done
   - 1: CSS descendent relationship selector is present, but incorrectly formed
   - 2: CSS descendent relationship selector is present, but no elements are actually selected
   - 3: CSS descendent relationship selector is present, but no more than one element is actually selected
   - 4: CSS descendent relationship selector is present, more than one element is selected

 - Style checking should not find any errors
   - 0: Several errors are present; some warnings may be present
   - 1: More than 1 error is present; some warnings may be present
   - 2: At least one error is present; some warnings may be present
   - 3: No errors present, but some warnings may be present
   - 4: No errors or warnings present