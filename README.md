Horiseon Webpage Accessibility Refactoring
==============
## Introduction
Horiseon Social Solution Services, Inc. seeks to increase accessibility of their webpage. This can be achieved in numerous ways that does not impact the style, format or performance of the site. By including more concise semantic HTML elements and adding attributes to links and images, the site will be optimized for search engines, screen readers and any other developer that may review the code.

## Examples

----

``` 
<div class="content">
    <div class="search-engine-optimization">
        <img src="./assets/images/search-engine-optimization.jpg" class="float-left"/>
            <h2>Search Engine Optimization</h2>
                <p>
                The dominance of mobile internet use means that users are searching for the right business as they travel, shop, or sit on their couch at home. Search Engine Optimization (SEO) allows you to increase your visibility and find the right customers for your business.
                </p>
    </div>
    ...
    ...
</div>
```

In this example of code you can see one `<div>` container followed by another `<div>` container. The initial `<div class=content>` element can be changed to a `<section>` element as it is parent to three other containers. The child elements can be changed to `<article>` elements so it is clear that there is some text in these areas.

<br>

Another issue with this section of code is the lack of an alt attribute regarding the embeded image. Puting an alt attribute in the image lets search engines and screen readers know what is on the page when it comes to a non-text item.

----

When using proper semantics and attributes for images this code will look like this:
```
<section class="content">
    <article id="search-engine-optimization" class="search-engine-optimization">
        <img src="./assets/images/search-engine-optimization.jpg" alt="Search Enginge Optimization" class="float-left" />
            <h2>Search Engine Optimization</h2>
                <p>
                The dominance of mobile internet use means that users are searching for the right business as they travel, shop, or sit on their couch at home. Search Engine Optimization (SEO) allows you to increase your visibility and find the right customers for your business.
                </p>
    </article>
    ...
    ...
</section>
```

Now there are more clearly defined containers and attrtibutes given to elements in this section of code. Additionally, there was an "id" attribute missing from the `<article>` element that rendered a link in the nav bar dead. The addition of this attribute increases the functionality of the site. This section of code is representative of changes that are necessary in every section of the page.

----

One unique, yet small accessibility hurdle in this site also lies in its footer. The heading "Made with ❤️ by Horiseon" may not be properly read by screen readers. The heart emoji could be read as "heart," "red heart," or "love." This can be fixed by a simple code wrap around the emoji.
```
<h4>Made with <span role=img aria-label="love">❤️</span>️ by Horiseon</h4>
```
This wrapping lets a screen reader know there is a non-text image within the element and that it should be read as "love" by a screen reader. Although most screen readers have good emoji compatability this makes it so there will be no doubt about the context of the above text.

----

## Appearance

![Demo](assets/images/Horiseon-Demo.png)

## Built Using
* HTML5
* CSS
* Git
* GitHub

----

## Deployed URL
[https://spenrad.github.io/Accessibility_Refactor/](https://spenrad.github.io/Accessibility_Refactor/)

----

## Author
Spencer Christy<br>
[GitHub](https://github.com/spenrad)<br>
[LinkedIn](https://www.linkedin.com/in/spencer-christy-543b84b3/)<br>

----

## Other Contributors
UC Berkeley Coding Bootcamp (initial build)

---

## Acknowledgments
Thank you for reading.