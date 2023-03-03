# John Doe HTML Single File Template

This is my version of the John Doe template (JD) by Gregory Cadars, a complete and simple website contained in a single HTML file including CSS, images and content, without JavaScript or external dependencies, occupying only 120 kB. 

Based on:

- [John Doe template by Gregory Cadars](http://github.com/cadars/john-doe/)
- [Zen Garden websites by Joost Schee](http://github.com/jhvanderschee/zengardenwebsites)
- [A Whole Website in a Single HTML File by Robin Rendle](http://css-tricks.com/a-whole-website-in-a-single-html-file)
- [John Doe question on Stackoverflow](http://stackoverflow.com/questions/66522759/how-exactly-does-the-css-in-the-john-doe-no-js-webpage-manage-to-make-the-defaul)
- and others

See the references above for more information.

What I tried to do was pack everything (CSS, images, data, HTML) into a single HTML file with no external dependencies, in such a way that there is only a single HTML file and nothing else. This lack of dependencies is often very convenient as it makes it impossible for the parts of an HTML to separate, and thus increases the chances of it still working in the future. It also doesn't use JavaScript, making it simple and small. This single file can be sent via email and viewed offline in a regular browser without the Internet, or it can be downloaded directly from the browser and viewed offline without losing functionality, and it can also be easily hosted on a cheap and simple web server.

The main john-doe.html file was edited using a text editor (I am using the [Kate](https://kate-editor.org/), but it could be, for example, an online editor like [htmlcodeeditor](https://htmlcodeeditor.com/) or [tutorialspoint](https://www.tutorialspoint.com/online_html_editor.php)). For convenience some pages were edited using [MarkText](https://github.com/marktext/marktext) which has the ability to copy and paste the HTML generated from markdown, however they could have been edited directly using HTML. The `.md` files generated by MarkText can be deleted when they are no longer needed, and in the future, if needed, [pandoc](https://pandoc.org/try/) or [htmlarkdown](https://evitanrelta.github.io/htmlmarkdown/) can be used to convert the HTML back to markdown.

For simplicity, the HTML file can be edited directly, and for example a post on the News page would look like this:

```html
<article>

<h2 id="20010101">Lorem ipsum
  <time datetime="2001-01-01">01.01.2001</time></h2>

<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim
veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea
commodo consequat.</p>

<p>Duis aute irure dolor in reprehenderit in voluptate velit esse cillum
dolore eu fugiat nulla pariatur.</p>

<p>Excepteur sint occaecat cupidatat non proident, sunt in culpa qui
officia deserunt mollit anim id est laborum.</p>

</article>
```

And the Markdown equivalent would be:

```markdown
<article>

<h2 id="20010101">Lorem ipsum
  <time datetime="2001-01-01">01.01.2001</time></h2>

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim
veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea
commodo consequat.

Duis aute irure dolor in reprehenderit in voluptate velit esse cillum
dolore eu fugiat nulla pariatur.

Excepteur sint occaecat cupidatat non proident, sunt in culpa qui
officia deserunt mollit anim id est laborum.

</article>
```

The difference is so small that, for simplicity, in this case it might not be worth using Markdown.

The external images were converted to the [base64](https://linux.die.net/man/1/base64) [webp](https://developers.google.com/speed/webp) format and inserted into the file as part of the HTML.

The example contained in the template has external links that appear with an arrow on the right side, in order to indicate an external link that can only be viewed in a browser with Internet access. This is important, for example, when browsing offline.

The John Doe template complies with Jeff Huang's 7 guidelines from [This Page is Designed to Last](https://jeffhuang.com/designed_to_last/):

1. Return to vanilla HTML/CSS
   - Does not have JavaScript, and passes the https://validator.w3.org/
2. Don't minimize that HTML
   - Neither the CSS nor the HTML is minimized and an attempt has also been made to comment out the HTML code to make it readable, although much can still be done to improve it
3. Prefer one page over several
   - It's a single HTML file and everything is inside this single file, there is no other external file
4. End all forms of hotlinking
   - There are no images from other websites, the CSS is part of the file and is not externally linked, it does not use Google Analytics, nor any type of hotlink
5. Stick with native fonts
   - There are no external fonts, and only generic font families are used
6. Obsessively compress your images
   - All example images contained in the template use webp format (converted to base64), and are at the minimum size
7. Eliminate the broken URL risk
   - At the moment the site is hosted on Github which I think is stable and will always be online, but using a monitoring service is always a good idea. And on the other hand, since it's a single HTML file, it can be easily downloaded and stored offline, so it should be relatively easy to preserve

What I find most interesting about JD is its simplicity. Being able to open a file using a simple text editor, make all the necessary changes, save and that's it. If I want to copy some part of another JD to mine, just open the 2 files, copy (Ctrl+C) and paste (Ctrl+V), save and that's it. And in the future when I need to use the file again, everything is in there, easy to find.

## Files

- john-doe_v0.1.html : original file with some minor fixes like links
- john-doe.html : single HTML file without external dependencies
- *.md : Markdown files used with MarkText that can be deleted if no longer needed


<p align="right">Last edited on 2023-02-25</p>
