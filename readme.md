# My Blawg: JS Selectors Practice

Open the included `index.html` in your browser.

# Part One: Vanilla JS

Write down how you would select the following DOM objects on "My Blawg". Use only the following methods or attributes:

- `querySelector`
- `querySelectorAll`
- `getElementById`
- `innerHTML`

---

1. The first `<a>` element on the page
//document.querySelector("a");

- All `<a>` elements on the page
//document.querySelectorAll("a");


- Using its ID, the `<h1>` at the top of the page
//document.getElementById('logo');

- All elements with class `post`
//document.querySelectorAll('.post');

- The first element with class `post`
//document.querySelector('post')[1];

- The second element with class `post`
//document.querySelector("p").innerHTML;

- The HTML content of the first `<p>` element on the page
//document.querySelector("p")[0]

# Part Two: jQuery

First, use a `<script>` tag in `index.html` to include the minified jQuery file in the `js` folder.

Then, write down how you would select the following DOM objects on "My Blawg". Use only the following methods or attributes:

- `$`
- `eq`
- `html`
//example:
jQuery("h2") or $("h2")- gives you all the h2

jQuery("h2").html(); -- gives you the first one's CONTENT if you want the actual element you'd have to do $(h2).eq(0);

jQuery("h2").html("Adrian") -- turns all the inner html inside the h2 to the word "Adrian"
---$ is the same things as "jQuery"

1. All `<a>` elements on the page
$("a")
- The first `<a>` element on the page
$("a").eq(0);
- Using an ID, the `<h1>` at the top of the page
$("#logo");  <-- whole element.
- All elements with class `post`
$(".post");
- The first element with class `post`
$(".post").eq(0);
- The second element with class `post`
$(".post").eq(2);
- The HTML content of the first `<a>` element on the page
$("a").html(); or $("a").eq(0).html();
- Using a CSS pseudo-selector, the third element with class `post`
$(".post:nth-child(3)"); ** CSS is indexed 1,2,3,4 NOT 0,1,2,3 *** psuedo-selectors in CSS are the ones that have a colon. :hover, :active,
- Using one of its HTML attributes, the fourth `<img>` on the page
$("img").eq(3); -- will return the 3rd image
$("[alt='balloons']") -- is using the attribute -- YOU HAVE TO USE SINGLE QUOTES in the BRACKETS

if you had ('[alt = "balloons"]') it would also work but you have to use the opposite quotes from inner or outer because JS will get confused.

# Part Three: Getting and Setting
 ** a "Getter" just returns the value
 ** a "Setter" changes it  
$("h2").css("background-color"); <-returns the value
$("h2").css("background-color", "red"); <--changes it

$("h2").prop("src"); <--getter
$("h2").prop("src", "url.in.quotes"); <---setter

Using these jQuery methods or attributes, follow the instructions below:

- `$`
- `eq`
- `html`
- `css`
- `prop`

Things to consider:
- What's the difference between `$("body").html()` and `$("body").html("hello")`? -- one will return the html content and the other will replace the content with whatever you pass to it.


- `$("p")` selects all `<p>` elements on the page.
  - If you run `$("p").html()`, how many elements' HTML does it return? the first one only. (to get more you'd do $("p")?

  - If you run `$("p").html('hello')"`, how many elements does it affect? all of them.
  - What about the other methods?

---

1. Get the HTML content of the second `<p>` element on the page
$("p").eq(1).html();

- Set the HTML content of the second `<p>` to something else weird
$("p").eq(1).html("Something Weird")

- Get the background color of the body
$("body").css("background-color");

- Set the background color of the body to "burlywood"
$("body").css("background-color", "burlywood");

- Get the `alt` value of the fourth `<img>` on the page
$("img").eq(3)prom("alt");

- Set the `alt` value of the fourth `<img>` on the page to "Why is my boat upside down?"
$("img").eq(3)prom("alt", "yard arm");
