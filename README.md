# Single file HTML website template

*Last edited: 2024-12-13*

It is a simple website template that allows you to create web pages using just one HTML file without external dependencies. It uses the `#anchor` suffix and the `:target` CSS selector to show and hide pages or content. To add a new page, you just need to add a section (`<section>`) with a unique ID and then create a link to that section in a navigation (`<nav>`).

* Template: https://efurlanm.github.io/john-doe
* Example: https://efurlanm.github.io/john-doe/profile.html

Based on:

- [John Doe template by Gregory Cadars](http://github.com/cadars/john-doe/)
- [Zen Garden websites by Joost Schee](http://github.com/jhvanderschee/zengardenwebsites)
- [A Whole Website in a Single HTML File by Robin Rendle](http://css-tricks.com/a-whole-website-in-a-single-html-file)
- [John Doe question on Stackoverflow](http://stackoverflow.com/questions/66522759/how-exactly-does-the-css-in-the-john-doe-no-js-webpage-manage-to-make-the-defaul)
- and others

(please see the references above for more information)

I tried to package everything (CSS, images, data, HTML) into a single HTML file with no external dependencies, so that there is only one HTML file that looks a bit like a DOCX file. It also uses no JavaScript, which makes it simple, small, fast, secure, and easy to edit by hand. This lack of dependencies is often very convenient, as it prevents the HTML pieces from becoming separated and therefore increases the chances that it will still work in the future, and it is also easy to handle, send via email, or host on a simple and cheap web server. It can be viewed offline in a regular browser without the Internet, or it can be easily downloaded directly from the browser, unlike traditional websites that use multiple external files. The CSS includes features for viewing on small smartphone screens.

The main file docs/index.html was edited using a text editor (I am using [Kate](https://kate-editor.org/), but it could be, for example, an online editor like [htmlcodeeditor](https://htmlcodeeditor.com/) or [tutorialspoint](https://www.tutorialspoint.com/online_html_editor.php)). For convenience some pages were edited using [MarkText](https://github.com/marktext/marktext) which has the ability to copy and paste the HTML generated from [Markdown](https://www.markdownguide.org/), however they could have been edited directly using HTML. If needed, [pandoc](https://pandoc.org/try/) or [htmlmarkdown](https://htmlmarkdown.com/) can be used to convert the HTML to Markdown. The images were converted to [base64](https://linux.die.net/man/1/base64) [webp](https://developers.google.com/speed/webp) format and inserted internally into the HTML file.

The template has external links that appear with an arrow on the right side, in order to indicate an external link that can only be viewed in a browser with Internet access. This is important, for example, when browsing offline.

The John Doe template complies with Jeff Huang's 7 guidelines from [This Page is Designed to Last](https://jeffhuang.com/designed_to_last/):

1. Return to vanilla HTML/CSS
      - Does not have JavaScript, and passes the https://validator.w3.org .
2. Don't minimize that HTML
      - Neither the CSS nor the HTML is minimized and an attempt has also been made to comment out the HTML code to make it readable, although much can still be done to improve it.
3. Prefer one page over several
      - It's a single HTML file and everything is inside this single file, there is no other external file.
4. End all forms of hotlinking
      - There are no images from other websites, the CSS is part of the file and is not externally linked, it does not use Google Analytics, nor any type of hotlink.
5. Stick with native fonts
      - There are no external fonts, and only generic font families are used.
6. Obsessively compress your images
      - All example images contained in the template use base64 webp format, and are at the minimum size.
7. Eliminate the broken URL risk
      - At the moment the site is hosted on Github which I think is stable and will always be online, but using a [monitoring service](https://geekflare.com/monitor-website-uptime/) is always a good idea. And on the other hand, since it's a single HTML file, it can be easily downloaded and stored offline, so it should be relatively easy to preserve.

What I found most interesting is its simplicity, being able to open a single file using a simple text editor, make all the necessary changes, save and that's it. If I want to copy some part of a file to another, just open them in any text editor, copy and paste, save and that's it. And in the future, when I need to change the file again, everything I need will be there inside the file. For small sites and simple pages, it's perfect.


## Files

- [docs/index.html](docs/index.html) - main single file HTML template.
- [docs/profile.html](docs/profile.html) - example based on [Nediyana's profile](https://nediyana.github.io)). The original html was converted to markdown (md) using [htmlmarkdown](https://htmlmarkdown.com). The md was edited using MarkText. The "Copy as HTML" feature was used to copy and paste into profile.html. The image was converted to base64 using [base64](https://askubuntu.com/questions/178521/how-can-i-decode-a-base64-string-from-the-command-line).
- [docs/profile.md](docs/profile.md) - the md file used in the MarText editor.
