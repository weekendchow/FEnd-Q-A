# HTML Questions

* [What does a doctype do?](#what-does-a-doctype-do)
* [How do you serve a page with content in multiple languages?](#how-do-you-serve-a-page-with-content-in-multiple-languages)
* [What kind of things must you be wary of when design or developing for multilingual sites?](#what-kind-of-things-must-you-be-wary-of-when-designing-or-developing-for-multilingual-sites)
* [What are `data-` attributes good for?](#what-are-data--attributes-good-for)
* [Consider HTML5 as an open web platform. What are the building blocks of HTML5?](#consider-html5-as-an-open-web-platform-what-are-the-building-blocks-of-html5)
* [Describe the difference between a `cookie`, `sessionStorage` and `localStorage`.](#describe-the-difference-between-a-cookie-sessionstorage-and-localstorage)
* [Describe the difference between `<script>`, `<script async>` and `<script defer>`.](#describe-the-difference-between-script-script-async-and-script-defer)
* [Why is it generally a good idea to position CSS `<link>`s between `<head></head>` and JS `<script>`s just before `</body>`? Do you know any exceptions?](#why-is-it-generally-a-good-idea-to-position-css-links-between-headhead-and-js-scripts-just-before-body-do-you-know-any-exceptions)
* [What is progressive rendering?](#what-is-progressive-rendering)
* [Why you would use a `srcset` attribute in an image tag? Explain the process the browser uses when evaluating the content of this attribute.](#why-you-would-use-a-srcset-attribute-in-an-image-tag-explain-the-process-the-browser-uses-when-evaluating-the-content-of-this-attribute)
* [Have you used different HTML templating languages before?](#have-you-used-different-html-templating-languages-before)


### What does a `DOCTYPE` do?

-	document type.
-	It is a declaration used in HTML to distinguish between **standards mode** and **quirks mode**(for the sake of maintaining backward compatibility).
-	Its presence tells the browser to render the web page in standards mode.

###### Reference
* https://stackoverflow.com/questions/7695044/what-does-doctype-html-do
* https://www.w3.org/QA/Tips/Doctype
* https://quirks.spec.whatwg.org/#history

[[↑] Back to top](#html-questions)


### How do you serve a page with content in multiple languages?

-	HTTP request sends information about language preferences to server.( Accept-Language header)
-	The server return a version of the document in the appropriate language.
-	The returned HTML document should also declare the *lang attribute* in the <html> tag, such as <html lang="en">...</html>.

-	In the back end, the HTML markup will contain *i18n* placeholders and content for the specific language stored in YML or JSON formats. The server then dynamically generates the HTML page with content in that particular language, usually with the help of a back end framework.

###### Reference
* https://www.w3.org/International/getting-started/language

[[↑] Back to top](#html-questions)


### What kind of things must you be wary of when designing or developing for multilingual sites?

-	**lang** attribute(<html lang="en">...</html>.)
-	options for user to **direct** the page to their native language - Allow a user to change his country/language easily without hassle.
-	**Text in images** is not a scalable approach - to translate image text, each string of text will need to have it's a separate image created for each language.
-	**Restrictive words/sentence length** - Some content can be longer when written in another language. Be wary of layout or overflow issues in the design. Character counts come into play with things like headlines, labels, and buttons. They are less of an issue with free-flowing text such as body text or comments.
-	Be mindful of how **colors** are perceived - Colors are perceived differently across languages and cultures.
-	Formatting **dates** and **currencies** - Eg. "May 31, 2012" in the U.S. vs. "31 May 2012" in parts of Europe.
-	**Do not concatenate** translated strings - Do not do anything like "The date today is " + date. It will break in languages with different word order. Use a template string with parameters substitution for each language instead. For example, look at the following two sentences in English and Chinese respectively: I will travel on {% date %} and {% date %} 我会出发. Note that the position of the variable is different due to grammar rules of the language.
-	Language **reading direction** - In English, we read from left-to-right, top-to-bottom, in traditional Japanese, text is read up-to-down, right-to-left.

###### Reference
* https://www.quora.com/What-kind-of-things-one-should-be-wary-of-when-designing-or-developing-for-multilingual-sites

[[↑] Back to top](#html-questions)


### What are `data-` attributes good for?

-	Before, it store extra data within the *DOM itself*.
-	It is intended to store **custom** data **private** to the page or application, for which there are no more appropriate attributes or elements.
-	These days, using data- attributes is not encouraged. users can *modify* the data attribute easily by using inspect element in the *browser*.
-	The data model is better stored within *JavaScript* itself and stay updated with the DOM via data binding possibly through a library or a framework.

###### Reference
* http://html5doctor.com/html5-custom-data-attributes/

[[↑] Back to top](#html-questions)


### Consider HTML5 as an open web platform. What are the building blocks of HTML5?

-	**Semantics** - Allowing you to describe more precisely what your content is. (p, nav, section, article, header, footer, aside)
-	**Connectivity** - Allowing you to communicate with the server in new and innovative ways.
-	**Offline and storage** - Allowing webpages to store data on the client-side locally and operate offline more efficiently.
-	**Multimedia** - Making video and audio first-class citizens in the Open Web. Embed them to the page (<audio><vedio>elements, webRTC, CameraAPI)
-	**2D/3D graphics and effects** - Allowing a much more diverse range of presentation options.<canvas>
-	**Performance and integration** - Providing greater speed optimization and better usage of computer hardware.(web worker, JIT, HistoryAPI, Drag&DropAPI, requestAnimationFrame, FullscreenAPI, PointerLockAPI)
-	**Device access** - Allowing for the usage of various input and output devices.(CameraAPI, geolocationAPI, LockAPI, Touch event, orientation)
-	**Styling** - Letting authors write more sophisticated themes.

###### Reference
* https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/HTML5

[[↑] Back to top](#html-questions)


### Describe the difference between a `cookie`, `sessionStorage` and `localStorage`.

- **key-value** storage mechanisms on the client side / Only ***strings***
#### `cookie`(4kb)
- Initiate on client or server(Set-Cookie header).
- **Manually** set expiry so the persistent across browser sessions depends.
- **Automatically** -> server(Cookie header).
- Access from any window.
#### `localStorage`(5MB)
- Initiate on client.
- **Never** expire and **persist** across browser.
- Do not -> server with every HTTP request.
- Access from any window.
#### `sessionStorage`(5MB)
- Initiate on client.
- Expire when **close the Tab** and do **not persist** across browser.
- Do not -> server with every HTTP request.
- Access on **same Tab**.

###### Reference
* https://developer.mozilla.org/en-US/docs/Web/HTTP/Cookies
* http://tutorial.techaltum.com/local-and-session-storage.html

[[↑] Back to top](#html-questions)


### Describe the difference between `<script>`, `<script async>` and `<script defer>`.

- `<script>`: HTML parsing is **blocked**, the script is fetched and executed **immediately**, HTML parsing **resumes** after the script is executed.
- `<script async>`: The script will be fetched in **parallel** to HTML parsing and executed **as soon as it is available** (potentially before HTML parsing completes). Use async when the script is **independent** of any other scripts on the page, for example, analytics.
- `<script defer>`:  The script will be fetched in **parallel** to HTML parsing and executed when the page has **finished parsing**. If there are multiple of them, each deferred script is executed **in the order** they were encoun­tered in the document. If a script relies on a fully-parsed DOM, the defer attribute will be useful in ensuring that the HTML is fully parsed before executing. There's not much difference in putting a normal <script> at the ***end of <body>***. A deferred script must ***not contain document.write***.
- Note: The async and defer attrib­utes are ignored for scripts that have no src attribute.


###### Reference
* http://www.growingwiththeweb.com/2014/02/async-vs-defer-attributes.html
* https://stackoverflow.com/questions/10808109/script-tag-async-defer
* https://bitsofco.de/async-vs-defer/

[[↑] Back to top](#html-questions)


### Why is it generally a good idea to position CSS `<link>`s between `<head></head>` and JS `<script>`s just before `</body>`? Do you know any exceptions?

- **Placing `<link>`s in the `<head>`**: Putting `<link>`s in the head is part of the **specification**. Besides that, placing at the top allows the page to **render progressively** which improves the user experience. It prevents the flash of unstyled contents.
- **Placing `<script>`s just before `</body>`**: `<script>`s block HTML parsing while they are being downloaded and executed. Downloading the scripts at the bottom will allow the HTML to be parsed and displayed to the user first.
- **Exceptions**: An exception for positioning of `<script>`s at the bottom is when your script contains document.write(), but these days it's not a good practice to use document.write(). Also, placing `<script>`s at the bottom means that the browser cannot start downloading the scripts until the entire document is parsed. One possible workaround is to put `<script>` in the `<head>` and use the defer attribute.

###### Reference
* https://developer.yahoo.com/performance/rules.html#css_top

[[↑] Back to top](#html-questions)


### What is progressive rendering?

- techniques used to improve the performance of a webpage (in particular, improve perceived load time) to render content for display as quickly as possible.
- It used to be much more prevalent in the days before broadband internet but it is still used in modern development as mobile data connections are becoming increasingly popular (and unreliable)!
#### Examples
- **Lazy loading** of images where (typically) some javascript will load an image when it comes into the browsers viewport instead of loading all images at page load.
- **Prioritizing visible content** (or above-the-fold rendering) - Include only the minimum CSS/content/scripts necessary for the amount of page that would be rendered in the users browser first to display as quickly as possible, you can then use ***deferred scripts*** or listen for the ***DOMContentLoaded/load*** event to load in other resources and content.

###### Reference
* https://stackoverflow.com/questions/33651166/what-is-progressive-rendering

[[↑] Back to top](#html-questions)


### Why you would use a `srcset` attribute in an image tag? Explain the process the browser uses when evaluating the content of this attribute.

- serve different images to users depending on their device display width
- serve smaller image files to narrow screen devices, as they don't need huge images like desktop displays do.
- serve different resolution images to high density/low-density screens.
- `<img srcset="small.jpg 500w, medium.jpg 1000w, large.jpg 2000w" src="..." alt="">`
For a device width of 320px, we have resolutions 500 / 320 = 1.5625, 1000 / 320 = 3.125, 2000 / 320 = 6.25. If the client's resolution is 1x, 1.5625 is the closest, choose small.jpg.
If resolution is 2x, choose medium.jpg

###### Reference
* https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images
* https://css-tricks.com/responsive-images-youre-just-changing-resolutions-use-srcset/

[[↑] Back to top](#html-questions)


### Have you used different HTML templating languages before?

- Yes, Pug (formerly Jade), ERB, Slim, Handlebars, Jinja, Liquid, just to name a few. In my opinion, they are more or less the same and provide similar functionality of escaping content and helpful filters for manipulating the data to be displayed. Most templating engines will also allow you to inject your own filters in the event you need custom processing before display.
