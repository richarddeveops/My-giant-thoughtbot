# Presentation Notes: Giant Robots Blog Page

## What the page does

This project recreates a simple blog page. It has a title and author introduction, a row of topic links, and a list of blog posts. The signup form and footer are not included.

## HTML tags in the page 

A tag is an HTML building block. The opening and closing tags mark where an element starts and ends.

| Tag | What it does here |
| --- | --- |
| `<!DOCTYPE html>` | Tells the browser to use modern HTML rules. |
| `<html lang="en">` | Wraps the page and says its language is English. |
| `<head>` | Holds page information that is not shown as page content. |
| `<meta>` | Gives the browser information such as the character set and mobile screen settings. |
| `<title>` | Sets the name shown in the browser tab. |
| `<link>` | Connects the HTML page to `style.css`. |
| `<body>` | Holds the content that appears on the page. |
| `<main>` | Marks the main content of the page. |
| `<header>` | Groups the page title and introduction at the top. |
| `<h1>` | The main heading. A page usually has one main `h1`. |
| `<h2>` | A heading for each blog post. |
| `<p>` | A paragraph of text. |
| `<a>` | Creates a link. The `href` attribute says where it goes. The `#` values here are placeholders, so these links do not go to real pages yet. |
| `<hr>` | Adds a horizontal dividing line. |
| `<div>` | A plain container used to group related content, such as one blog post. |
| `<ul>` | Creates a list with bullets by default. CSS changes the topic list into a horizontal row. |
| `<li>` | One item in a list, such as one topic link. |

Most of these tags were already in your original HTML. The main structural change was putting each post into its own `<div class="post">` so the posts can be styled consistently.

## Classes and CSS selectors

A class is a name added to an HTML element so CSS can style it. For example, `class="post"` lets the CSS select all post containers.

- `.post` styles each blog post.
- `.toPic` styles the list of topics.
- `.selected` gives the "All Topics" link its yellow background.
- `.moreTopics` gives "More topics" a dotted underline without a pill border.
- `.tags` styles the article topic labels in white.
- `.moreSpace` adds a larger gap before the second post. It leaves whitespace where the signup form used to appear without adding the form.

A dot at the start of a CSS selector means it selects a class. For example, `.post` selects elements with `class="post"`.

## CSS ideas used

- `*` is the universal selector. It selects every element. The first rule removes default spacing and makes element widths easier to control with `box-sizing: border-box`.
- `main { width: 90%; max-width: 760px; margin: 50px auto; }` keeps the content centered. It uses most of a small screen but does not grow too wide on a large screen. `auto` on the left and right margins centers it.
- `display: flex` puts the topic links in a row. `flex-wrap: wrap` lets them move onto another line on a narrow screen.
- `gap` sets the space between the topic links. The small-screen rule makes that gap smaller on phones.
- `border-radius` rounds the topic links into pill shapes. `padding` adds space inside them.
- `.post.moreSpace` selects an element that has both classes: `post` and `moreSpace`. The `margin-top` adds outside space above that post.
- `.post:last-child` uses `:last-child`, a special selector for the last child element. It puts a bottom line only at the end of the post list.
- `@media (max-width: 600px)` is a media query. It applies the rules inside it when the screen is 600 pixels wide or narrower, making the page easier to read on a phone.
- `color` changes text color, `background-color` changes the fill color, and `font-size` changes text size.

The topic row uses the existing `<ul>` and `<li>` tags. It is not a separate site navigation bar.

## Short presentation script

"I made a simple blog page using HTML for the content and CSS for the appearance. Each blog post is grouped in a div with the post class, which lets me give all the posts consistent spacing. The topic list is still a regular HTML list, but Flexbox displays its items in a row. I used a media query to make the layout fit smaller screens. I left out the signup form and footer, and used extra spacing where the signup form would have been."
